---
UID: NE:structuredquery.tagSTRUCTURED_QUERY_SINGLE_OPTION
title: STRUCTURED_QUERY_SINGLE_OPTION (structuredquery.h)
description: A set of flags to be used with IQueryParser::SetOption and IQueryParser::GetOption to indicate individual options.
helpviewer_keywords: ["SQSO_AUTOMATIC_WILDCARD","SQSO_CONNECTOR_CASE","SQSO_IMPLICIT_CONNECTOR","SQSO_LANGUAGE_KEYWORDS","SQSO_LOCALE_WORD_BREAKING","SQSO_NATURAL_SYNTAX","SQSO_SCHEMA","SQSO_SYNTAX","SQSO_TIME_ZONE","SQSO_TRACE_LEVEL","SQSO_WORD_BREAKER","STRUCTURED_QUERY_SINGLE_OPTION","STRUCTURED_QUERY_SINGLE_OPTION enumeration [search]","_search_STRUCTURED_QUERY_SINGLE_OPTION","search._search_STRUCTURED_QUERY_SINGLE_OPTION","structuredquery/SQSO_AUTOMATIC_WILDCARD","structuredquery/SQSO_CONNECTOR_CASE","structuredquery/SQSO_IMPLICIT_CONNECTOR","structuredquery/SQSO_LANGUAGE_KEYWORDS","structuredquery/SQSO_LOCALE_WORD_BREAKING","structuredquery/SQSO_NATURAL_SYNTAX","structuredquery/SQSO_SCHEMA","structuredquery/SQSO_SYNTAX","structuredquery/SQSO_TIME_ZONE","structuredquery/SQSO_TRACE_LEVEL","structuredquery/SQSO_WORD_BREAKER","structuredquery/STRUCTURED_QUERY_SINGLE_OPTION"]
old-location: search\_search_STRUCTURED_QUERY_SINGLE_OPTION.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\structured_query_single_option.htm
ms.date: 12/05/2018
ms.keywords: SQSO_AUTOMATIC_WILDCARD, SQSO_CONNECTOR_CASE, SQSO_IMPLICIT_CONNECTOR, SQSO_LANGUAGE_KEYWORDS, SQSO_LOCALE_WORD_BREAKING, SQSO_NATURAL_SYNTAX, SQSO_SCHEMA, SQSO_SYNTAX, SQSO_TIME_ZONE, SQSO_TRACE_LEVEL, SQSO_WORD_BREAKER, STRUCTURED_QUERY_SINGLE_OPTION, STRUCTURED_QUERY_SINGLE_OPTION enumeration [search], _search_STRUCTURED_QUERY_SINGLE_OPTION, search._search_STRUCTURED_QUERY_SINGLE_OPTION, structuredquery/SQSO_AUTOMATIC_WILDCARD, structuredquery/SQSO_CONNECTOR_CASE, structuredquery/SQSO_IMPLICIT_CONNECTOR, structuredquery/SQSO_LANGUAGE_KEYWORDS, structuredquery/SQSO_LOCALE_WORD_BREAKING, structuredquery/SQSO_NATURAL_SYNTAX, structuredquery/SQSO_SCHEMA, structuredquery/SQSO_SYNTAX, structuredquery/SQSO_TIME_ZONE, structuredquery/SQSO_TRACE_LEVEL, structuredquery/SQSO_WORD_BREAKER, structuredquery/STRUCTURED_QUERY_SINGLE_OPTION
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STRUCTURED_QUERY_SINGLE_OPTION
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - tagSTRUCTURED_QUERY_SINGLE_OPTION
 - structuredquery/tagSTRUCTURED_QUERY_SINGLE_OPTION
 - STRUCTURED_QUERY_SINGLE_OPTION
 - structuredquery/STRUCTURED_QUERY_SINGLE_OPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Structuredquery.h
api_name:
 - STRUCTURED_QUERY_SINGLE_OPTION
---

# STRUCTURED_QUERY_SINGLE_OPTION enumeration


## -description

A set of flags to be used with <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-setoption">IQueryParser::SetOption</a> and <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-getoption">IQueryParser::GetOption</a> to indicate individual options.

## -enum-fields

### -field SQSO_SCHEMA:0

The option value should be a <b>VT_LPWSTR</b> that is the path to a file containing a schema binary. It is set automatically when obtaining a query parser through <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparsermanager-createloadedparser">IQueryParserManager::CreateLoadedParser</a>.

### -field SQSO_LOCALE_WORD_BREAKING

The option value must be <b>VT_EMPTY</b> to use the default word breaker (current keyboard locale) or a <b>VT_UI4</b> that is a valid LCID. The LCID indicates the expected locale of content words in queries to be parsed and is used to choose a suitable word breaker for the query. <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-parse">IQueryParser::Parse</a> will return an error unless you set either this option or <a href="/windows/desktop/api/structuredquery/ne-structuredquery-structured_query_single_option">SQSO_WORD_BREAKER</a>  before calling it.

### -field SQSO_WORD_BREAKER

When setting this option, the value should be a <b>VT_EMPTY</b> for using the default word breaker for the chosen locale, or a <b>VT_UNKNOWN</b> with an object supporting the <a href="/windows/desktop/api/indexsrv/nn-indexsrv-iwordbreaker">IWordBreaker</a> interface. Retrieving the option always returns a <b>VT_UNKNOWN</b> with an object supporting the <b>IWordBreaker</b> interface, unless there is no suitable word breaker for the chosen locale, in which case <b>VT_EMPTY</b> is returned.

### -field SQSO_NATURAL_SYNTAX

The option value should be a <b>VT_EMPTY</b> or a <b>VT_BOOL</b> with <b>VARIANT_TRUE</b> to allow both natural query syntax and advanced query syntax (the default) or a <b>VT_BOOL</b> with <b>VARIANT_FALSE</b> to allow only advanced query syntax. Retrieving the option always returns a <b>VT_BOOL</b>.

### -field SQSO_AUTOMATIC_WILDCARD

The option value should be a <b>VT_BOOL</b> with <b>VARIANT_TRUE</b> to generate query expressions as if each word in the query had the wildcard character * appended to it (unless followed by punctuation other than a parenthesis), a <b>VT_BOOL</b> with <b>VARIANT_FALSE</b> to use the words as they are (the default), or a <b>VT_EMPTY</b>. In most cases, a word-wheeling application should set this option to <b>VARIANT_TRUE</b>. Retrieving the option always returns a <b>VT_BOOL</b>.

### -field SQSO_TRACE_LEVEL

Reserved. The value should be <b>VT_EMPTY</b> (the default) or a <b>VT_I4</b>. Retrieving the option always returns a <b>VT_I4</b>.

### -field SQSO_LANGUAGE_KEYWORDS

The option value must be a <b>VT_I4</b> that is a valid LANGID. The LANGID indicates the expected language of Structured Query keywords in queries to be parsed. It is set automatically when obtaining a query parser through <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparsermanager-createloadedparser">IQueryParserManager::CreateLoadedParser</a>.

### -field SQSO_SYNTAX

<b>Windows 7 and later.</b> The option value must be a <b>VT_UI4</b> that is a <a href="/windows/desktop/api/searchapi/ne-searchapi-search_query_syntax">SEARCH_QUERY_SYNTAX</a> value. The default is SQS_NATURAL_QUERY_SYNTAX.

### -field SQSO_TIME_ZONE

<b>Windows 7 and later.</b> The value must be a <b>VT_BLOB</b> that is a copy of a TIME_ZONE_INFORMATION structure. The default is the current time zone.

### -field SQSO_IMPLICIT_CONNECTOR

<b>Windows 7 and later.</b> This setting decides what connector should be assumed between conditions when none is specified. The value must be a <b>VT_UI4</b> that is a CONDITION_TYPE. Only CT_AND_CONDITION and CT_OR_CONDITION are valid. It defaults to CT_AND_CONDITION.

### -field SQSO_CONNECTOR_CASE

<b>Windows 7 and later.</b> This setting decides whether there are special requirements on the case of connector keywords (such as AND or OR). The value must be a <b>VT_UI4</b> that is a CASE_REQUIREMENT value. It defaults to CASE_REQUIREMENT_UPPER_IF_AQS.

## -remarks

Windows 7 adds new constants that help refine query condition trees parsed by the <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iqueryparser">IQueryParser</a> interface.
