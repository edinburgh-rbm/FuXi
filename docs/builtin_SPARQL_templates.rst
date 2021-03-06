==============================================================================
Builtin SPARQL Templates 
==============================================================================

Introduction
===============================


Describes how N3 builtins can be cast into SPARQL filters so they can be
solved along with other literals in the body of a rule as a large group.

In converting builtins into SPARQL FILTERs, a user-specified template
can be provided for this purpose. An example of how this can be done is
below. The format for this SPARQL FILER template specification is in
RDF:

::

    @prefix templ:  <http://code.google.com/p/fuxi/wiki/BuiltinSPARQLTemplates#>.
    @prefix owl:    <http://www.w3.org/2002/07/owl#>.
    @prefix owl:    <http://www.w3.org/2002/07/owl#>.
    @prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#>.
    @prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#>.
    @prefix str:    <http://www.w3.org/2000/10/swap/string#>.
    @prefix log:    <http://www.w3.org/2000/10/swap/log#>.
    @prefix math:   <http://www.w3.org/2000/10/swap/math#>.

    str:greaterThan          templ:filterTemplate "STR(%s) > STR(%s)" .
    log:notEqualTo           templ:filterTemplate "%s != %s" .
    str:startsWith           templ:filterTemplate "REGEX(%s,'$%s')" .
    str:greaterThanOrEqualTo templ:filterTemplate "STR(%s) >= STR(%s)" .
    str:lessThanOrEqualTo    templ:filterTemplate "STR(%s) <= STR(%s)" .


