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

# MI_Instance_GetElement function


## -description


Gets the value of the named element (CIM property).


## -parameters




### -param self [in]

Instance whose element value will be returned.


### -param name

A null-terminated string that represents the name of the element.


### -param value [out, optional]

Returned element value.


### -param type [out, optional]

Returned element value type.


### -param flags [out, optional]

Returned combination of the following values.



#### MI_FLAG_NULL (0x20000000)

Element value is <b>Null</b>.



#### MI_FLAG_KEY (0x0001000)

Element is a key.



#### MI_FLAG_IN (0x0002000)

The parameter is of type <b>In</b> and is passed into a method.



#### MI_FLAG_OUT (0x0004000)

The parameter is of type <b>Out</b> and is returned from a method.


### -param index [out, optional]

Returned zero-based index of the element.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/51a26894-f391-4281-9e06-2e70fb662aa2">MI_Instance_AddElement</a>



<a href="https://msdn.microsoft.com/de945902-4b10-47d1-a374-a1aeab02a787">MI_Instance_ClearElement</a>



<a href="https://msdn.microsoft.com/581f8d9f-5421-44ab-a3e2-dfb536a35c2c">MI_Instance_SetElement</a>
 

 

