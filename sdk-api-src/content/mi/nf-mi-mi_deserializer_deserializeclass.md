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

# MI_Deserializer_DeserializeClass function


## -description


Deserializes a serialized buffer into an <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> object.


## -parameters




### -param deserializer [in, out]

A pointer to a deserializer object returned from a call to <a href="https://msdn.microsoft.com/e58c69ce-032a-4024-9023-53cd1776b7f3">MI_Application_NewDeserializer</a>.  The deserializer must match the serializer that created the buffer.


### -param flags

This parameter must be 0.


### -param serializedBuffer

A serialized buffer that was filled via a call from <a href="https://msdn.microsoft.com/3417731d-8727-4dcb-8ce4-2b07b6addd19">MI_Serializer_SerializeClass</a>.


### -param serializedBufferLength

The length of the buffer that was reported via a call to <a href="https://msdn.microsoft.com/3417731d-8727-4dcb-8ce4-2b07b6addd19">MI_Serializer_SerializeClass</a>.


### -param parentClass [in, optional]

The parent class. If the class was not serialized with the class's parent class then this parameter needs to contain the <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> for the parent class.  The parent class needs to contain all parent classes in the hierarchy.  If the class was serialized with <b>MI_SERIALIZER_FLAGS_CLASS_DEEP</b> specified as a flag, then the parent class is not needed as it is a self-contained buffer, and <b>NULL</b> can be passed for this parameter.


### -param serverName

An optional, null-terminated string that represents the server name.


### -param namespaceName

An optional, null-terminated string that represents the namespace name.


### -param classObjectNeeded [in, optional]

A callback function used to provide a requested class object during deserialization.


### -param classObjectNeededContext [in, out]

A pointer to the context that is used with the callback function.


### -param serializedBufferRead [out, optional]

The amount of the serialized buffer that was read (deserialized).


### -param classObject

The returned deserialized class.  This class needs to be deleted via <a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a>.


### -param cimErrorDetails

If the call fails, this value will contain information useful in debugging. This value must be deleted via <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>.


## -returns



This function returns MI_INLINE MI_Result.




## -see-also




<a href="https://msdn.microsoft.com/0C813AAF-99B4-4DA7-9C2F-CD9FA146D7D2">MI_Deserializer_ClassObjectNeeded</a>
 

 

