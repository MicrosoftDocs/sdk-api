---
UID: NE:searchapi._SEARCH_QUERY_SYNTAX
title: "_SEARCH_QUERY_SYNTAX"
author: windows-sdk-content
description: Specifies the type of query syntax.
old-location: search\_search_SEARCH_QUERY_SYNTAX.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\search_query_syntax.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: SEARCH_ADVANCED_QUERY_SYNTAX, SEARCH_NATURAL_QUERY_SYNTAX, SEARCH_NO_QUERY_SYNTAX, SEARCH_QUERY_SYNTAX, SEARCH_QUERY_SYNTAX enumeration [search], _SEARCH_QUERY_SYNTAX, _search_SEARCH_QUERY_SYNTAX, search._search_SEARCH_QUERY_SYNTAX, searchapi/SEARCH_ADVANCED_QUERY_SYNTAX, searchapi/SEARCH_NATURAL_QUERY_SYNTAX, searchapi/SEARCH_NO_QUERY_SYNTAX, searchapi/SEARCH_QUERY_SYNTAX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SEARCH_QUERY_SYNTAX
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - SEARCH_QUERY_SYNTAX
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _SEARCH_QUERY_SYNTAX enumeration


## -description


Specifies the type of query syntax. 


## -enum-fields




### -field SEARCH_NO_QUERY_SYNTAX


        No syntax.
      


### -field SEARCH_ADVANCED_QUERY_SYNTAX


      Specifies the Advanced Query Syntax. For example, "kind:email to:david to:bill".
      


### -field SEARCH_NATURAL_QUERY_SYNTAX


      Specifies the Natural Query Syntax. This syntax removes the requirement for a colon between properties and values, for example, "email from david to bill".
      


## -remarks



This enumerated type is used by the <a href="https://msdn.microsoft.com/72802fbc-6684-40e3-9df5-a81e2c4bc1c2">ISearchQueryHelper::get_QuerySyntax</a> and <a href="https://msdn.microsoft.com/4df77a77-10fd-411c-bd35-450ffdbc1da8">ISearchQueryHelper::put_QuerySyntax</a> methods.

<div class="alert"><b>Note</b>   In Windows 7, the names are prefixed with SQS_ instead of SEARCH_.</div>
<div> </div>


