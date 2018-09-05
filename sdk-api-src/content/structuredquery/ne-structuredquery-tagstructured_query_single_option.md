---
UID: NE:structuredquery.tagSTRUCTURED_QUERY_SINGLE_OPTION
title: tagSTRUCTURED_QUERY_SINGLE_OPTION
author: windows-sdk-content
description: A set of flags to be used with IQueryParser::SetOption and IQueryParser::GetOption to indicate individual options.
old-location: search\_search_STRUCTURED_QUERY_SINGLE_OPTION.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\structured_query_single_option.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: SQSO_AUTOMATIC_WILDCARD, SQSO_CONNECTOR_CASE, SQSO_IMPLICIT_CONNECTOR, SQSO_LANGUAGE_KEYWORDS, SQSO_LOCALE_WORD_BREAKING, SQSO_NATURAL_SYNTAX, SQSO_SCHEMA, SQSO_SYNTAX, SQSO_TIME_ZONE, SQSO_TRACE_LEVEL, SQSO_WORD_BREAKER, STRUCTURED_QUERY_SINGLE_OPTION, STRUCTURED_QUERY_SINGLE_OPTION enumeration [search], _search_STRUCTURED_QUERY_SINGLE_OPTION, search._search_STRUCTURED_QUERY_SINGLE_OPTION, structuredquery/SQSO_AUTOMATIC_WILDCARD, structuredquery/SQSO_CONNECTOR_CASE, structuredquery/SQSO_IMPLICIT_CONNECTOR, structuredquery/SQSO_LANGUAGE_KEYWORDS, structuredquery/SQSO_LOCALE_WORD_BREAKING, structuredquery/SQSO_NATURAL_SYNTAX, structuredquery/SQSO_SCHEMA, structuredquery/SQSO_SYNTAX, structuredquery/SQSO_TIME_ZONE, structuredquery/SQSO_TRACE_LEVEL, structuredquery/SQSO_WORD_BREAKER, structuredquery/STRUCTURED_QUERY_SINGLE_OPTION, tagSTRUCTURED_QUERY_SINGLE_OPTION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: structuredquery.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchVPrintf_lW (Unicode) and StringCchVPrintf_lA (ANSI)
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STRUCTURED_QUERY_SINGLE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Structuredquery.h
api_name:
 - STRUCTURED_QUERY_SINGLE_OPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# tagSTRUCTURED_QUERY_SINGLE_OPTION enumeration


## -description


A set of flags to be used with <a href="https://msdn.microsoft.com/a7c2d4d7-7ccf-4daa-b4d5-cf23ed1e88b4">IQueryParser::SetOption</a> and <a href="https://msdn.microsoft.com/85216ad7-6988-43cd-87b3-49a2ca1173b6">IQueryParser::GetOption</a> to indicate individual options.


## -enum-fields




### -field SQSO_SCHEMA

The option value should be a <b>VT_LPWSTR</b> that is the path to a file containing a schema binary. It is set automatically when obtaining a query parser through <a href="https://msdn.microsoft.com/22ae21a0-927e-4e76-856e-7285e4abfea3">IQueryParserManager::CreateLoadedParser</a>.


### -field SQSO_LOCALE_WORD_BREAKING

The option value must be <b>VT_EMPTY</b> to use the default word breaker (current keyboard locale) or a <b>VT_UI4</b> that is a valid LCID. The LCID indicates the expected locale of content words in queries to be parsed and is used to choose a suitable word breaker for the query. <a href="https://msdn.microsoft.com/2ca6ddfa-821c-4d84-abbf-61d25b633180">IQueryParser::Parse</a> will return an error unless you set either this option or <a href="https://msdn.microsoft.com/2753f0ad-2648-4ec2-b53f-089caad8ec15">SQSO_WORD_BREAKER</a>  before calling it.


### -field SQSO_WORD_BREAKER

When setting this option, the value should be a <b>VT_EMPTY</b> for using the default word breaker for the chosen locale, or a <b>VT_UNKNOWN</b> with an object supporting the <a href="https://msdn.microsoft.com/36c46931-5c5c-4ab9-9291-60ad93cebbf0">IWordBreaker</a> interface. Retrieving the option always returns a <b>VT_UNKNOWN</b> with an object supporting the <b>IWordBreaker</b> interface, unless there is no suitable word breaker for the chosen locale, in which case <b>VT_EMPTY</b> is returned.


### -field SQSO_NATURAL_SYNTAX

The option value should be a <b>VT_EMPTY</b> or a <b>VT_BOOL</b> with <b>VARIANT_TRUE</b> to allow both natural query syntax and advanced query syntax (the default) or a <b>VT_BOOL</b> with <b>VARIANT_FALSE</b> to allow only advanced query syntax. Retrieving the option always returns a <b>VT_BOOL</b>.


### -field SQSO_AUTOMATIC_WILDCARD

The option value should be a <b>VT_BOOL</b> with <b>VARIANT_TRUE</b> to generate query expressions as if each word in the query had the wildcard character * appended to it (unless followed by punctuation other than a parenthesis), a <b>VT_BOOL</b> with <b>VARIANT_FALSE</b> to use the words as they are (the default), or a <b>VT_EMPTY</b>. In most cases, a word-wheeling application should set this option to <b>VARIANT_TRUE</b>. Retrieving the option always returns a <b>VT_BOOL</b>.


### -field SQSO_TRACE_LEVEL

Reserved. The value should be <b>VT_EMPTY</b> (the default) or a <b>VT_I4</b>. Retrieving the option always returns a <b>VT_I4</b>.


### -field SQSO_LANGUAGE_KEYWORDS

The option value must be a <b>VT_I4</b> that is a valid LANGID. The LANGID indicates the expected language of Structured Query keywords in queries to be parsed. It is set automatically when obtaining a query parser through <a href="https://msdn.microsoft.com/22ae21a0-927e-4e76-856e-7285e4abfea3">IQueryParserManager::CreateLoadedParser</a>.


### -field SQSO_SYNTAX

<b>Windows 7 and later.</b> The option value must be a <b>VT_UI4</b> that is a <a href="https://msdn.microsoft.com/a0331339-9df0-4190-b7ae-977572b49c2d">SEARCH_QUERY_SYNTAX</a> value. The default is SQS_NATURAL_QUERY_SYNTAX.


### -field SQSO_TIME_ZONE

<b>Windows 7 and later.</b> The value must be a <b>VT_BLOB</b> that is a copy of a TIME_ZONE_INFORMATION structure. The default is the current time zone.


### -field SQSO_IMPLICIT_CONNECTOR

<b>Windows 7 and later.</b> This setting decides what connector should be assumed between conditions when none is specified. The value must be a <b>VT_UI4</b> that is a CONDITION_TYPE. Only CT_AND_CONDITION and CT_OR_CONDITION are valid. It defaults to CT_AND_CONDITION.


### -field SQSO_CONNECTOR_CASE

<b>Windows 7 and later.</b> This setting decides whether there are special requirements on the case of connector keywords (such as AND or OR). The value must be a <b>VT_UI4</b> that is a CASE_REQUIREMENT value. It defaults to CASE_REQUIREMENT_UPPER_IF_AQS. 


## -remarks



Windows 7 adds new constants that help refine query condition trees parsed by the <a href="https://msdn.microsoft.com/f022464d-9db6-42c8-a3fb-12c31ec48756">IQueryParser</a> interface.



