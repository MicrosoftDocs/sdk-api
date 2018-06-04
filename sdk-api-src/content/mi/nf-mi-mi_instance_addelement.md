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

# MI_Instance_AddElement function


## -description


Adds a new property to a dynamic instance (supported only by dynamic instances whose schema may be extended at run time).


## -parameters




### -param self [in, out]

Instance to which the element will be added.


### -param name

A null-terminated string that represents the name of the new element.


### -param value [in, optional]

Element value.


### -param type

Element type.


### -param flags

Flags of the new element that can be a combination of the following flag values.



#### MI_FLAG_KEY (0x00001000)

Element is a key.



#### MI_FLAG_IN (0x00002000)

Parameter is of type In and is passed into a method.



#### MI_FLAG_OUT (0x00004000)

Parameter is of type Out and is returned from a method.



#### MI_FLAG_REQUIRED (0x00008000)

Parameter is required.



#### MI_FLAG_STREAM (0x00100000)

Method parameter will be streamed back to the client from the provider.



#### MI_FLAG_BORROW (0x4000000)

Used while adding and setting properties on an <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> to indicate that the instance will not copy the value. The value must stay valid until the instance is deleted.



#### MI_FLAG_ADOPT (0x8000000)

Used while adding and setting properties on an <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> to indicate that the instance will adopt the pointer and will be responsible for deleting it.



#### MI_FLAG_NULL (0x2000000)

Element value is <b>Null</b>.



#### MI_FLAG_ANY (0x0000007F)

Bitmask used to filter out other flags.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -see-also




<a href="https://msdn.microsoft.com/de945902-4b10-47d1-a374-a1aeab02a787">MI_Instance_ClearElement</a>



<a href="https://msdn.microsoft.com/1e366cc5-0fb9-41c9-961c-07b076a18529">MI_Instance_GetElement</a>



<a href="https://msdn.microsoft.com/581f8d9f-5421-44ab-a3e2-dfb536a35c2c">MI_Instance_SetElement</a>
 

 

