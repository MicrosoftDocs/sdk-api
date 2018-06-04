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


