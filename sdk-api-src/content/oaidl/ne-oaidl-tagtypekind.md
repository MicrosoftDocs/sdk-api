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

# tagTYPEKIND enumeration


## -description


Specifies a type.


## -enum-fields




### -field TKIND_ENUM

A set of enumerators.



### -field TKIND_RECORD

A structure with no methods.



### -field TKIND_MODULE

A module that can only have static functions and data (for example, a DLL).



### -field TKIND_INTERFACE

A type that has virtual and pure functions.



### -field TKIND_DISPATCH

A set of methods and properties that are accessible through <a href="https://msdn.microsoft.com/964ade8e-9d8a-4d32-bd47-aa678912a54d">IDispatch::Invoke</a>. By default, dual interfaces return TKIND_DISPATCH.



### -field TKIND_COCLASS

A set of implemented component object interfaces.



### -field TKIND_ALIAS

A type that is an alias for another type.



### -field TKIND_UNION

A union, all of whose members have an offset of zero.



### -field TKIND_MAX

End of enum marker.

