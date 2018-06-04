---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



