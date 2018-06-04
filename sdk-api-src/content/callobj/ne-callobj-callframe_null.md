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

# CALLFRAME_NULL enumeration


## -description


Determines the parameter type to be freed.


## -enum-fields




### -field CALLFRAME_NULL_NONE

No values are freed.


### -field CALLFRAME_NULL_INOUT

The data referenced by [in, out] parameters are freed.


### -field CALLFRAME_NULL_OUT

The data referenced by [out] parameters are freed. 


### -field CALLFRAME_NULL_ALL

All [out] and [in, out] parameters are freed. 


## -see-also




<a href="https://msdn.microsoft.com/97261d93-40cf-4a27-9bee-677600c04699">ICallFrame::Free</a>
 

 

