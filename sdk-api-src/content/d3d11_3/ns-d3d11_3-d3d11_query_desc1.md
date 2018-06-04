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

# D3D11_QUERY_DESC1 structure


## -description


Describes a query.


## -struct-fields




#### - Query

A <a href="https://msdn.microsoft.com/4161fbeb-7f58-422c-a195-ea10f737fd0c">D3D11_QUERY</a>-typed value that specifies the type of query.


#### - MiscFlags

A combination of <a href="https://msdn.microsoft.com/a49a04f9-5804-43fb-b12d-f703721f4d30">D3D11_QUERY_MISC_FLAG</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies query behavior.




#### - ContextType

A <a href="https://msdn.microsoft.com/5467F07C-E429-4324-B52E-FDC25B4DB9FE">D3D11_CONTEXT_TYPE</a>-typed value that specifies the context for the query.


## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

