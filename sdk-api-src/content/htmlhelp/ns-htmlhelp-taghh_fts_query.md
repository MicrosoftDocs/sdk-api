---
UID: NS:htmlhelp.tagHH_FTS_QUERY
title: tagHH_FTS_QUERY
author: windows-sdk-content
description: Use this structure for full-text search.
old-location: htmlhelp\hh_fts_query_structure.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\vsconstrhhftsquery.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: HH_FTS_QUERY, HH_FTS_QUERY structure [HTML Help Workshop], htmlhelp.hh_fts_query_structure, htmlhelp/HH_FTS_QUERY, tagHH_FTS_QUERY, vsconStrhhftsquery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: htmlhelp.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: HH_FTS_QUERY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HtmlHelp.h
api_name:
 - HH_FTS_QUERY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagHH_FTS_QUERY structure


## -description


Use this structure for full-text search. 


## -struct-fields




### -field cbStruct

Specifies the size of the structure. 


### -field fUniCodeStrings

TRUE if all strings are Unicode. 


### -field pszSearchQuery

String containing the search query. 


### -field iProximity

Word proximity. 


### -field fStemmedSearch

TRUE for StemmedSearch only. 


### -field fTitleOnly

TRUE for Title search only. 


### -field fExecute

TRUE to initiate the search. 


### -field pszWindow

Window to display in. 


## -see-also




<a href="https://msdn.microsoft.com/E75CA82E-9759-47d8-AF84-5842EDAB019D">About Structures</a>
 

 

