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

# MI_Deserializer_Class_GetParentClassName function


## -description


Gets the parent class name from a serialized class buffer.


## -parameters




### -param deserializer [in, out]

A pointer to a deserializer object returned from a call to <a href="https://msdn.microsoft.com/e58c69ce-032a-4024-9023-53cd1776b7f3">MI_Application_NewDeserializer</a>.  The deserializer must match the serializer that created the buffer.


### -param serializedBuffer

A serialized buffer that was filled via a call from <a href="https://msdn.microsoft.com/45c5033a-b2ef-4fb6-a09e-54b3cd9fc99f">MI_Serializer_SerializeInstance</a>.


### -param serializedBufferLength

The length of the buffer that was reported via a call to <a href="https://msdn.microsoft.com/45c5033a-b2ef-4fb6-a09e-54b3cd9fc99f">MI_Serializer_SerializeInstance</a>.


### -param parentClassName

Returned parent class name.  If this parameter is <b>Null</b>, the required buffer size is returned through the <i>parentClassNameLength</i> parameter.


### -param parentClassNameLength [in, out]

A pointer to  the length of the <i>parentClassName</i> buffer.  If <i>parentClassName</i> is <b>NULL</b>, this parameter is filled in with the required length of the buffer needed.


### -param cimErrorDetails

If the call fails, this value will contain information useful in debugging. This value must be deleted via <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



Not all serializers include enough information to retrieve this information, in which case the function will fail with a <b>MI_RESULT_NOT_SUPPORTED</b> error.  If no parent exists, the function will return a <b>MI_RESULT_NOT_FOUND</b> error.



