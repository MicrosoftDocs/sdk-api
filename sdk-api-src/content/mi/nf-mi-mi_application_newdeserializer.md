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

# MI_Application_NewDeserializer function


## -description


Creates a deserializer object that can then be used to convert a serialized object back into a class 
    or instance.


## -parameters




### -param application [in, out]

Handle returned from 
      <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a>.


### -param flags

Must be 0.


### -param format [in]

A string that indicates which serializer to use. Must be L"MI_XML".


### -param deserializer [out]

The populated deserializer object.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



Serializers are used to persist <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> and 
    <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> objects to <b>BYTE</b> arrays. 
    A deserializer is then used to re-create the object from its stored form.



