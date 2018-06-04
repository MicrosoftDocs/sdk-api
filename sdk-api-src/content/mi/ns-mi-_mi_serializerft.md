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

# _MI_SerializerFT structure


## -description


A support structure used in the 
     <a href="https://msdn.microsoft.com/9c8c812d-d91d-4754-9be5-c05360364b1b">MI_ClientFT_V1</a> structure. Use the functions with the 
     name prefix "MI_Serializer_" to manipulate these structures.


## -struct-fields






#### - Close

Closes a serializer object and frees any internal memory associated with it. See 
       <a href="https://msdn.microsoft.com/fbae767d-1f30-4b73-8978-ea14ce707303">MI_Serializer_Close</a>.


#### - SerializeClass

Serializes an <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> into a buffer in the format 
       specified when it was created. See 
       <a href="https://msdn.microsoft.com/3417731d-8727-4dcb-8ce4-2b07b6addd19">MI_Serializer_SerializeClass</a>.


#### - SerializeInstance

Serializes an <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> into a buffer in the 
       format specified when the serializer was created. See 
       <a href="https://msdn.microsoft.com/45c5033a-b2ef-4fb6-a09e-54b3cd9fc99f">MI_Serializer_SerializeInstance</a>.

