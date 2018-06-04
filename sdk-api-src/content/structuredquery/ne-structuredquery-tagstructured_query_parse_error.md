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

# tagSTRUCTURED_QUERY_PARSE_ERROR enumeration


## -description


A set of flags to be used with <a href="https://msdn.microsoft.com/50eead1a-5eb9-4bc9-ba54-c6dc77284f4d">IQuerySolution::GetErrors</a> to indentify parsing error(s). Each parsing error indicates that one or more tokens were ignored when parsing a query string.


## -enum-fields




### -field SQPE_NONE

No error.


### -field SQPE_EXTRA_OPENING_PARENTHESIS

An extraneous <b>(</b>.


### -field SQPE_EXTRA_CLOSING_PARENTHESIS

An extraneous <b>)</b>.


### -field SQPE_IGNORED_MODIFIER

An extraneous <b>NOT</b>, <b>&lt;</b>, <b>&gt;</b>, <b>=</b>, and so forth.


### -field SQPE_IGNORED_CONNECTOR

An extraneous <b>AND</b> or <b>OR</b>.


### -field SQPE_IGNORED_KEYWORD

A property or other keyword used in the wrong context.


### -field SQPE_UNHANDLED

Any other parse error.


## -see-also




<a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a>
 

 

