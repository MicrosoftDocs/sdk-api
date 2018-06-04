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

# MI_Instance_GetElementAt function


## -description


Gets the value of the element (CIM property) at the specified index.


## -parameters




### -param self [in]

Instance whose element value will be returned.


### -param index

Zero-based index of the element


### -param name

A pointer to a null-terminated string containing the returned element name.


### -param value [out, optional]

Returned element value.


### -param type [out, optional]

Returned element type.


### -param flags [out, optional]

Returned combination of the following values.



#### MI_FLAG_NULL (0x2000000)

Element value is <b>Null</b>.



#### MI_FLAG_KEY (0x0001000)

Element is a key.



#### MI_FLAG_IN (0x0002000)

The parameter is of type <b>In</b> and is passed into a method.



#### MI_FLAG_OUT (0x0004000)

The parameter is of type <b>Out</b> and is returned from a method.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>



<a href="https://msdn.microsoft.com/ef97bfa4-2e06-44b1-aa50-ce8c6a550c69">MI_Instance_ClearElementAt</a>



<a href="https://msdn.microsoft.com/a378bde1-c164-4905-82f8-f771f8da60ba">MI_Instance_GetElementCount</a>



<a href="https://msdn.microsoft.com/4070af24-b7f9-4484-ab13-d3a52c9e55a0">MI_Instance_SetElementAt</a>
 

 

