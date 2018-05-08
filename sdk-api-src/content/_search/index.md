---
UID: TP:search
ms.assetid: b29ae40f-9b92-3070-8037-b6c4cfdc20bc
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Windows Search



Overview of the Windows Search technology.

To develop Windows Search, you need these headers:

 * [filtereg.h](..\filtereg\index.md)
 * [shobjidl_core.h](..\shobjidl_core\index.md)
 * [structuredquery.h](..\structuredquery\index.md)
 * [structuredquerycondition.h](..\structuredquerycondition\index.md)
 * [subsmgr.h](..\subsmgr\index.md)

For the programming guide, see [Windows Search](https://review.docs.microsoft.com/en-us/win32-test/search).

## Structures

| Title   | Description   |
| ---- |:---- |
| [_FILTERED_DATA_SOURCES structure](..\filtereg\ns-filtereg-_filtered_data_sources.md) | Specifies parameters for a Shell data source for which a filter is loaded. |
| [_tagITEMPROP structure](..\subsmgr\ns-subsmgr-_tagitemprop.md) | Stores information about properties in the Windows Property System, and is used by the IItemPropertyBag interface. |
| [tagHITRANGE structure](..\structuredquery\ns-structuredquery-taghitrange.md) | Identifies the range of matching data when query search conditions match indexed data. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [CASE_REQUIREMENT enumeration](..\structuredquery\ne-structuredquery-case_requirement.md) | Specifies the case requirements of keywords, if any, for a query. |
| [CONDITION_CREATION_OPTIONS enumeration](..\structuredquery\ne-structuredquery-condition_creation_options.md) | Provides a set of flags to be used with the following interfaces to indicate the type of condition tree node |
| [STRUCTURED_QUERY_RESOLVE_OPTION enumeration](..\structuredquery\ne-structuredquery-structured_query_resolve_option.md) | Options for resolving data into a condition tree. |
| [__MIDL___MIDL_itf_structuredquery_0000_0012_0001 enumeration](..\structuredquery\ne-structuredquery-__midl___midl_itf_structuredquery_0000_0012_0001.md) | Defines the level of certainty for a named entity. |
| [tagCONDITION_OPERATION enumeration](..\structuredquerycondition\ne-structuredquerycondition-tagcondition_operation.md) | Provides a set of flags to be used with following methods to indicate the operation in ICondition |
| [tagCONDITION_TYPE enumeration](..\structuredquerycondition\ne-structuredquerycondition-tagcondition_type.md) | Provides a set of flags to be used with the following methods to indicate the type of condition tree node |
| [tagINTERVAL_LIMIT_KIND enumeration](..\structuredquery\ne-structuredquery-taginterval_limit_kind.md) | These values are returned by IInterval |
| [tagQUERY_PARSER_MANAGER_OPTION enumeration](..\structuredquery\ne-structuredquery-tagquery_parser_manager_option.md) | Used by IQueryParserManager |
| [tagSTRUCTURED_QUERY_MULTIOPTION enumeration](..\structuredquery\ne-structuredquery-tagstructured_query_multioption.md) | A set of flags used by IQueryParser |
| [tagSTRUCTURED_QUERY_PARSE_ERROR enumeration](..\structuredquery\ne-structuredquery-tagstructured_query_parse_error.md) | A set of flags to be used with IQuerySolution |
| [tagSTRUCTURED_QUERY_SINGLE_OPTION enumeration](..\structuredquery\ne-structuredquery-tagstructured_query_single_option.md) | A set of flags to be used with IQueryParser |
| [tagSTRUCTURED_QUERY_SYNTAX enumeration](..\structuredquery\ne-structuredquery-tagstructured_query_syntax.md) | Specifies the type of query syntax. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [ICondition interface](..\structuredquerycondition\nn-structuredquerycondition-icondition.md) | Provides methods for retrieving information about a search condition. |
| [ICondition2 interface](..\structuredquerycondition\nn-structuredquerycondition-icondition2.md) | Extends the functionality of the ICondition interface. ICondition2 provides methods for retrieving information about a search condition. |
| [IConditionFactory interface](..\structuredquery\nn-structuredquery-iconditionfactory.md) | Provides methods for creating or resolving a condition tree that was obtained by parsing a query string. |
| [IConditionFactory2 interface](..\structuredquery\nn-structuredquery-iconditionfactory2.md) | Extends the functionality of IConditionFactory. IConditionFactory2 provides methods for creating or resolving a condition tree that was obtained by parsing a query string. |
| [IConditionGenerator interface](..\structuredquery\nn-structuredquery-iconditiongenerator.md) | Provides methods for handling named entities and generating special conditions. |
| [IEntity interface](..\structuredquery\nn-structuredquery-ientity.md) | Provides methods for retrieving information about an entity type in the schema. |
| [IInterval interface](..\structuredquery\nn-structuredquery-iinterval.md) | Provides a method to get the limits of an interval. |
| [ILoadFilter interface](..\filtereg\nn-filtereg-iloadfilter.md) | Defines methods and properties that are implemented by the FilterRegistration object, which provides methods for loading a filter. |
| [IMetaData interface](..\structuredquery\nn-structuredquery-imetadata.md) | Provides a method for retrieving a key/value pair of strings from an IEntity, IRelationship or ISchemaProvider object. |
| [INamedEntity interface](..\structuredquery\nn-structuredquery-inamedentity.md) | Provides methods to get the value of, or a default phrase for the value of, a named entity. |
| [INamedEntityCollector interface](..\structuredquery\nn-structuredquery-inamedentitycollector.md) | Provides a method to accumulate named entities as identified by an IConditionGenerator object. |
| [IQueryParser interface](..\structuredquery\nn-structuredquery-iqueryparser.md) | Provides methods to parse an input string into an IQuerySolution object. |
| [IQueryParserManager interface](..\structuredquery\nn-structuredquery-iqueryparsermanager.md) | Provides methods to create, initialize, and change options for an IQueryParser object. |
| [IQuerySolution interface](..\structuredquery\nn-structuredquery-iquerysolution.md) | Provides methods that retrieve information about the interpretation of a parsed query. |
| [IRelationship interface](..\structuredquery\nn-structuredquery-irelationship.md) | Provides methods for retrieving information about a schema property. |
| [IRichChunk interface](..\structuredquerycondition\nn-structuredquerycondition-irichchunk.md) | Represents a chunk of data as a string and a PROPVARIANT value. |
| [ISchemaLocalizerSupport interface](..\structuredquery\nn-structuredquery-ischemalocalizersupport.md) | Provides a method for localizing keywords in a specified string. |
| [ISchemaProvider interface](..\structuredquery\nn-structuredquery-ischemaprovider.md) | Provides a schema repository that can be browsed. |
| [ITokenCollection interface](..\structuredquery\nn-structuredquery-itokencollection.md) | Gets the tokens that result from using a word breaker. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [ICondition2::GetLeafConditionInfo](..\structuredquerycondition\nf-structuredquerycondition-icondition2-getleafconditioninfo.md) | Retrieves the property name, operation, and value from a leaf search condition node. |
| [ICondition2::GetLocale](..\structuredquerycondition\nf-structuredquerycondition-icondition2-getlocale.md) | Retrieves the property name, operation, and value from a leaf search condition node. |
| [ICondition::Clone](..\structuredquerycondition\nf-structuredquerycondition-icondition-clone.md) | Creates a deep copy of this ICondition object. |
| [ICondition::GetComparisonInfo](..\structuredquerycondition\nf-structuredquerycondition-icondition-getcomparisoninfo.md) | Retrieves the property name, operation, and value from a leaf search condition node. |
| [ICondition::GetConditionType](..\structuredquerycondition\nf-structuredquerycondition-icondition-getconditiontype.md) | Retrieves the condition type for this search condition node, identifying it as a logical AND, OR, or NOT, or as a leaf node. |
| [ICondition::GetInputTerms](..\structuredquerycondition\nf-structuredquerycondition-icondition-getinputterms.md) | For a leaf node, ICondition |
| [ICondition::GetSubConditions](..\structuredquerycondition\nf-structuredquerycondition-icondition-getsubconditions.md) | Retrieves a collection of the subconditions of the search condition node and the IID of the interface for enumerating the collection. |
| [ICondition::GetValueNormalization](..\structuredquerycondition\nf-structuredquerycondition-icondition-getvaluenormalization.md) | Retrieves the character-normalized value of the search condition node. |
| [ICondition::GetValueType](..\structuredquerycondition\nf-structuredquerycondition-icondition-getvaluetype.md) | Retrieves the semantic type of the value of the search condition node. |
| [IConditionFactory2::CreateBooleanLeaf](..\structuredquery\nf-structuredquery-iconditionfactory2-createbooleanleaf.md) | Creates a search condition that is either TRUE or FALSE. |
| [IConditionFactory2::CreateCompoundFromArray](..\structuredquery\nf-structuredquery-iconditionfactory2-createcompoundfromarray.md) | Creates a leaf condition node that is a conjunction (AND) or a disjunction (OR) from an array of condition nodes. The returned object supports ICondition and ICondition2. |
| [IConditionFactory2::CreateCompoundFromObjectArray](..\structuredquery\nf-structuredquery-iconditionfactory2-createcompoundfromobjectarray.md) | Creates a leaf condition node that is a conjunction (AND) or a disjunction (OR) of a collection of subconditions. The returned object supports ICondition and ICondition2. |
| [IConditionFactory2::CreateIntegerLeaf](..\structuredquery\nf-structuredquery-iconditionfactory2-createintegerleaf.md) | Creates a leaf condition node for an integer value. The returned object supports ICondition and ICondition2. |
| [IConditionFactory2::CreateLeaf](..\structuredquery\nf-structuredquery-iconditionfactory2-createleaf.md) | Creates a leaf condition node for any value. The returned object supports ICondition and ICondition2. |
| [IConditionFactory2::CreateNegation](..\structuredquery\nf-structuredquery-iconditionfactory2-createnegation.md) | Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node). |
| [IConditionFactory2::CreateStringLeaf](..\structuredquery\nf-structuredquery-iconditionfactory2-createstringleaf.md) | Creates a leaf condition node for a string value that represents a comparison of property value and constant value. The returned object supports ICondition and ICondition2. |
| [IConditionFactory2::CreateTrueFalse](..\structuredquery\nf-structuredquery-iconditionfactory2-createtruefalse.md) | Creates a search condition that is either TRUE or FALSE. |
| [IConditionFactory2::ResolveCondition](..\structuredquery\nf-structuredquery-iconditionfactory2-resolvecondition.md) | Performs a variety of transformations on a condition tree, and thereby the resolved condition for evaluation. The returned object supports ICondition and ICondition2. |
| [IConditionFactory::MakeAndOr](..\structuredquery\nf-structuredquery-iconditionfactory-makeandor.md) | Creates a condition node that is a logical conjunction (AND) or disjunction (OR) of a collection of subconditions. |
| [IConditionFactory::MakeLeaf](..\structuredquery\nf-structuredquery-iconditionfactory-makeleaf.md) | Creates a leaf condition node that represents a comparison of property value and constant value. |
| [IConditionFactory::MakeNot](..\structuredquery\nf-structuredquery-iconditionfactory-makenot.md) | Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node). |
| [IConditionFactory::Resolve](..\structuredquery\nf-structuredquery-iconditionfactory-resolve.md) | Performs a variety of transformations on a condition tree, including the following |
| [IConditionGenerator::DefaultPhrase](..\structuredquery\nf-structuredquery-iconditiongenerator-defaultphrase.md) | This method attempts to produce a phrase that, when recognized by this instance of IConditionGenerator, represents the type and value pair for an entity, relationship, or named entity. |
| [IConditionGenerator::GenerateForLeaf](..\structuredquery\nf-structuredquery-iconditiongenerator-generateforleaf.md) | Generates a special query expression for what would otherwise become a leaf query expression. |
| [IConditionGenerator::Initialize](..\structuredquery\nf-structuredquery-iconditiongenerator-initialize.md) | Resets all states of the interface to default values and retrieves any necessary information from the schema. |
| [IConditionGenerator::RecognizeNamedEntities](..\structuredquery\nf-structuredquery-iconditiongenerator-recognizenamedentities.md) | Identifies named entities in an input string, and creates a collection containing them. |
| [IEntity::Base](..\structuredquery\nf-structuredquery-ientity-base.md) | Retrieves the parent entity of this entity. |
| [IEntity::DefaultPhrase](..\structuredquery\nf-structuredquery-ientity-defaultphrase.md) | Retrieves a default phrase to use for this entity in restatements. |
| [IEntity::GetNamedEntity](..\structuredquery\nf-structuredquery-ientity-getnamedentity.md) | Retrieves an INamedEntity object based on an entity name. |
| [IEntity::GetRelationship](..\structuredquery\nf-structuredquery-ientity-getrelationship.md) | Retrieves the IRelationship object for this entity as requested by name. |
| [IEntity::MetaData](..\structuredquery\nf-structuredquery-ientity-metadata.md) | Retrieves an enumeration of IMetaData objects for this entity. |
| [IEntity::Name](..\structuredquery\nf-structuredquery-ientity-name.md) | Retrieves the name of this entity. |
| [IEntity::NamedEntities](..\structuredquery\nf-structuredquery-ientity-namedentities.md) | Retrieves an enumeration of INamedEntity objects, one for each known named entity of this type. |
| [IEntity::Relationships](..\structuredquery\nf-structuredquery-ientity-relationships.md) | Retrieves an enumeration of IRelationship objects, one for each relationship this entity has. |
| [IInterval::GetLimits](..\structuredquery\nf-structuredquery-iinterval-getlimits.md) | Specifies the lower and upper limits of an interval, each of which may be infinite or a specific value. |
| [ILoadFilter::LoadIFilter](..\filtereg\nf-filtereg-iloadfilter-loadifilter.md) | Retrieves and loads the most appropriate filter that is mapped to a Shell data source. |
| [IMetaData::GetData](..\structuredquery\nf-structuredquery-imetadata-getdata.md) | Retrieves one key/value pair from the metadata of an IEntity, IRelationship, or ISchemaProvider object. |
| [INamedEntity::DefaultPhrase](..\structuredquery\nf-structuredquery-inamedentity-defaultphrase.md) | Retrieves a default phrase to use for this named entity in restatements. |
| [INamedEntity::GetValue](..\structuredquery\nf-structuredquery-inamedentity-getvalue.md) | Retrieves the value of this named entity as a string. |
| [INamedEntityCollector::Add](..\structuredquery\nf-structuredquery-inamedentitycollector-add.md) | Adds a single (potential) named entity to this INamedEntityCollector collection, as identified in a tokenized span of the input string being parsed. |
| [IQueryParser::GetOption](..\structuredquery\nf-structuredquery-iqueryparser-getoption.md) | Retrieves a specified simple option value for this query parser. |
| [IQueryParser::GetSchemaProvider](..\structuredquery\nf-structuredquery-iqueryparser-getschemaprovider.md) | Retrieves a schema provider for browsing the currently loaded schema. |
| [IQueryParser::ParsePropertyValue](..\structuredquery\nf-structuredquery-iqueryparser-parsepropertyvalue.md) | Parses a condition for a specified property. |
| [IQueryParser::Parse](..\structuredquery\nf-structuredquery-iqueryparser-parse.md) | Parses an input string that contains Structured Query keywords and/or contents to produce an IQuerySolution object. |
| [IQueryParser::RestatePropertyValueToString](..\structuredquery\nf-structuredquery-iqueryparser-restatepropertyvaluetostring.md) | Restates a specified property for a condition as a query string. |
| [IQueryParser::RestateToString](..\structuredquery\nf-structuredquery-iqueryparser-restatetostring.md) | Restates a condition as a structured query string. If the condition was the result of parsing an original query string, the keywords of that query string are used to a great extent. If not, default keywords are used. |
| [IQueryParser::SetMultiOption](..\structuredquery\nf-structuredquery-iqueryparser-setmultioption.md) | Sets a complex option, such as a specified condition generator, to use when parsing an input string. |
| [IQueryParser::SetOption](..\structuredquery\nf-structuredquery-iqueryparser-setoption.md) | Sets a single option, such as a specified wordbreaker, for parsing an input string. |
| [IQueryParserManager::CreateLoadedParser](..\structuredquery\nf-structuredquery-iqueryparsermanager-createloadedparser.md) | Creates a new instance of a IQueryParser interface implementation. This instance of the query parser is loaded with the schema for the specified catalog and is localized to a specified language. All other settings are initialized to default settings. |
| [IQueryParserManager::InitializeOptions](..\structuredquery\nf-structuredquery-iqueryparsermanager-initializeoptions.md) | Sets the flags for Natural Query Syntax (NQS) and automatic wildcard characters for the specified query parser. |
| [IQueryParserManager::SetOption](..\structuredquery\nf-structuredquery-iqueryparsermanager-setoption.md) | Changes a single option in this IQueryParserManager object. For example, this method could change the name of the schema binary to load or the location of localized schema binaries. |
| [IQuerySolution::GetErrors](..\structuredquery\nf-structuredquery-iquerysolution-geterrors.md) | Identifies parts of the input string that the parser did not recognize or did not use when constructing the IQuerySolution condition tree. |
| [IQuerySolution::GetLexicalData](..\structuredquery\nf-structuredquery-iquerysolution-getlexicaldata.md) | Reports the query string, how it was tokenized, and what language code identifier (LCID) and word breaker were used to parse it. |
| [IQuerySolution::GetQuery](..\structuredquery\nf-structuredquery-iquerysolution-getquery.md) | Retrieves the condition tree and the semantic type of the solution. |
| [IRelationship::DefaultPhrase](..\structuredquery\nf-structuredquery-irelationship-defaultphrase.md) | Retrieves the default phrase to use for this relationship in restatements. |
| [IRelationship::Destination](..\structuredquery\nf-structuredquery-irelationship-destination.md) | Retrieves the destination IEntity object of the relationship. The destination of a relationshipo corresponds to the type of a property. |
| [IRelationship::IsReal](..\structuredquery\nf-structuredquery-irelationship-isreal.md) | Reports whether a relationship is real. |
| [IRelationship::MetaData](..\structuredquery\nf-structuredquery-irelationship-metadata.md) | Retrieves an enumeration of IMetaData objects for this relationship. |
| [IRelationship::Name](..\structuredquery\nf-structuredquery-irelationship-name.md) | Retrieves the name of the relationship. |
| [IRichChunk::GetData](..\structuredquerycondition\nf-structuredquerycondition-irichchunk-getdata.md) | Retrieves the PROPVARIANT and input string that represents a chunk of data. |
| [ISchemaLocalizerSupport::Localize](..\structuredquery\nf-structuredquery-ischemalocalizersupport-localize.md) | Localizes keywords from an input string. |
| [ISchemaProvider::Entities](..\structuredquery\nf-structuredquery-ischemaprovider-entities.md) | Retrieves an enumeration of IEntity objects with one entry for each entity in the loaded schema. |
| [ISchemaProvider::GetEntity](..\structuredquery\nf-structuredquery-ischemaprovider-getentity.md) | Retrieves an entity by name from the loaded schema. |
| [ISchemaProvider::Localize](..\structuredquery\nf-structuredquery-ischemaprovider-localize.md) | Localizes the currently loaded schema for a specified locale. |
| [ISchemaProvider::LookupAuthoredNamedEntity](..\structuredquery\nf-structuredquery-ischemaprovider-lookupauthorednamedentity.md) | Finds named entities of a specified type in a tokenized string, and returns the value of the entity and the number of tokens the entity value occupies. |
| [ISchemaProvider::MetaData](..\structuredquery\nf-structuredquery-ischemaprovider-metadata.md) | Retrieves an enumeration of global IMetaData objects for the loaded schema. |
| [ISchemaProvider::RootEntity](..\structuredquery\nf-structuredquery-ischemaprovider-rootentity.md) | Retrieves the root entity of the loaded schema. |
| [ISchemaProvider::SaveBinary](..\structuredquery\nf-structuredquery-ischemaprovider-savebinary.md) | Saves the loaded schema as a schema binary at a specified path. |
| [ITokenCollection::GetToken](..\structuredquery\nf-structuredquery-itokencollection-gettoken.md) | Retrieves the position, length, and any overriding string of an individual token. |
| [ITokenCollection::NumberOfTokens](..\structuredquery\nf-structuredquery-itokencollection-numberoftokens.md) | Retrieves the number of tokens in the collection. |
