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

# tagFUNCKIND enumeration


## -description


Specifies the function type.


## -enum-fields




### -field FUNC_VIRTUAL

The function is accessed the same as PUREVIRTUAL, except the function has an implementation.


### -field FUNC_PUREVIRTUAL

The function is accessed through the virtual function table (VTBL), and takes an implicit this pointer.


### -field FUNC_NONVIRTUAL

The function is accessed by static address and takes an implicit this pointer.



### -field FUNC_STATIC

The function is accessed by static address and does not take an implicit this pointer.



### -field FUNC_DISPATCH

The function can be accessed only through <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>.


