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

# _MI_DeserializerFT structure


## -description


A support structure used in the 
     <a href="https://msdn.microsoft.com/9c8c812d-d91d-4754-9be5-c05360364b1b">MI_ClientFT_V1</a> structure. Use the functions with the 
     name prefix "MI_Deserializer_" to manipulate these structures.


## -struct-fields






#### - Class_GetClassName

Gets the class name from a serialized class buffer. See 
       <a href="https://msdn.microsoft.com/a4dc8992-ccdf-4883-a37d-83cb6d8da53a">MI_Deserializer_Class_GetClassName</a>.


#### - Class_GetParentClassName

Gets the parent class name from a serialized class buffer. See 
       <a href="https://msdn.microsoft.com/35e1d864-cc81-466e-bc5b-006c0aaf56fc">MI_Deserializer_Class_GetParentClassName</a>.


#### - Close

Deletes the deserializer object and its associated memory. See 
       <a href="https://msdn.microsoft.com/34ddbd4f-723f-4580-aad6-c5c236a1f5d9">MI_Deserializer_Close</a>.


#### - DeserializeClass

Deserializes a serialized buffer into an <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> 
       object. See 
       <a href="https://msdn.microsoft.com/09ad196c-9940-4d10-8a4e-1e06acd5d677">MI_Deserializer_DeserializeClass</a>.


#### - DeserializeInstance

Deserializes a serialized buffer into a 
       <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> object. See 
       <a href="https://msdn.microsoft.com/54b24a50-f700-4369-b6dc-8406000a5b30">MI_Deserializer_DeserializeInstance</a>.


#### - Instance_GetClassName

Gets the class name of the specified instance. See 
       <a href="https://msdn.microsoft.com/d2129902-3a2d-479d-b83a-3582094b2fce">MI_Instance_GetClassName</a>.


## -see-also




<a href="https://msdn.microsoft.com/0C813AAF-99B4-4DA7-9C2F-CD9FA146D7D2">MI_Deserializer_ClassObjectNeeded</a>
 

 

