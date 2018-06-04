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

# MI_Serializer_SerializeClass function


## -description


Serializes an <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> into a buffer in the format specified when the serializer was created.  Options can be passed into the flags to control if the class and all its parent classes are serialized, or just the child-most class.


## -parameters




### -param serializer [in, out]

Serializer returned from <a href="https://msdn.microsoft.com/9de29d43-0677-4dc9-927f-af7c01179991">MI_Application_NewSerializer</a>.


### -param flags

Must be either 0 or <b>MI_SERIALIZER_FLAGS_CLASS_DEEP</b>. 0 means only the child most part of the class will be serialized. <b>MI_SERIALIZER_FLAGS_CLASS_DEEP</b> means all properties in the class will be serialized.


### -param classObject [in]

Class object to be serialized.


### -param clientBuffer

The output buffer to receive the serialized class data.  If this parameter is <b>Null</b>, the required length of the buffer is passed back in <i>clientBufferNeeded</i>.


### -param clientBufferLength

Length of the <i>clientBuffer</i> passed in.  If <i>clientBuffer</i> is <b>Null</b>, this parameter should be 0.


### -param clientBufferNeeded [in, out]

Returned total length the buffer needs to be.  If a buffer is passed in (via the <i>clientBuffer</i> parameter) that is the required size or more, this value will indicate how much buffer was used.  If a buffer was not passed in (where the <i>clientBuffer</i> value is <b>Null</b>) or the buffer is too small to hold the serialized class, this value will indicate how much space is needed to hold the serialized class.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/9de29d43-0677-4dc9-927f-af7c01179991">MI_Application_NewSerializer</a>
 

 

