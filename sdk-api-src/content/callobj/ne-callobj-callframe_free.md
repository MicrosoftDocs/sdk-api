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

# CALLFRAME_FREE enumeration


## -description


Determines the parameter type to be freed.


## -enum-fields




### -field CALLFRAME_FREE_NONE

No values are freed.


### -field CALLFRAME_FREE_IN

The [in] parameters are freed. This includes both top-level pointers and the data they reference.


### -field CALLFRAME_FREE_INOUT

The data referenced by [in, out] parameters are freed. However, the top-level pointers, which are the actual parameter values, are not freed.

On the server side, this is typically used post-call, as in CALLFRAME_FREE_IN. On the client side, this is typically used when the server was not actually invoked (and so unmarshaling of return values was not attempted) or when unmarshaling of the return values failed. 


### -field CALLFRAME_FREE_OUT

The data referenced by [out] parameters are freed. However, the top-level pointers, which are the actual parameter values, are not freed.

On the server side, this is typically used post-call, as in CALLFRAME_FREE_IN. On the client side, this is typically only used when unmarshaling of return values failed.


### -field CALLFRAME_FREE_TOP_INOUT

The [in, out] parameters are freed. This includes both top-level pointers and the data they reference.


### -field CALLFRAME_FREE_TOP_OUT

The [out] parameters are freed. This includes both top-level pointers and the data they reference.


### -field CALLFRAME_FREE_ALL

All [in], [out], and [in, out] parameters are freed. This includes both top-level pointers and the data they reference.



## -see-also




<a href="https://msdn.microsoft.com/97261d93-40cf-4a27-9bee-677600c04699">ICallFrame::Free</a>



<a href="https://msdn.microsoft.com/b141bfc4-de1b-4251-b88f-551d0805e9b6">ICallFrame::FreeParam</a>
 

 

