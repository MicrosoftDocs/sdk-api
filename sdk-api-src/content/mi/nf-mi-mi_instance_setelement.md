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

# MI_Instance_SetElement function


## -description


Set the value of the element with the given name in the given instance.


## -parameters




### -param self [out]

A pointer to an instance.


### -param name

A null-terminated string that represents the name of the element that will be set.


### -param value [in, optional]

The new value for the element.


### -param type

The CIM type of the element that will be set.


### -param flags

Bit flags indicating memory management policy.



#### MI_FLAG_BORROW

Used while adding and setting properties on an <b>MI_Instance</b> to indicate that the instance will not copy the value. The value must stay valid until the instance is deleted.



#### MI_FLAG_ADOPT

Used while adding and setting properties on an <b>MI_Instance</b> to indicate that the instance will adopt the pointer and will be responsible for deleting it.



#### MI_FLAG_NULL

Element value is <b>Null</b>.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



By default, all memory referred to by the value parameter is copied. By passing the flag MI_FLAG_BORROW, memory pointers within the value structure are stored directly in the instance's element. The caller must guarantee that the memory outlives the instance.



