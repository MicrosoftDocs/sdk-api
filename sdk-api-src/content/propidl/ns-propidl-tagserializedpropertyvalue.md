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

# tagSERIALIZEDPROPERTYVALUE structure


## -description


A range of memory of arbitrary type that represents a serialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. Programs should not inspect the contents of a <b>SERIALIZEDPROPERTYVALUE</b>; instead, they should manipulate it with the <a href="https://msdn.microsoft.com/c588e239-616f-4569-88b5-6bfb504cefa1">StgSerializePropVariant</a> and <a href="https://msdn.microsoft.com/0517ef4d-e57c-4613-8d11-5e1eb14eb9fa">StgDeserializePropVariant</a> functions.


## -struct-fields




### -field dwType

Type: <b>DWORD</b>

Encodes type information about the serialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. Programs should not inspect this member directly; instead, they should use the <a href="https://msdn.microsoft.com/0517ef4d-e57c-4613-8d11-5e1eb14eb9fa">StgDeserializePropVariant</a> function and inspect the <b>vt</b>  member of the resulting <b>PROPVARIANT</b> structure.


### -field rgb

Type: <b>BYTE[1]</b>

A variable-length additional data that depends on the type passed in <b>dwType</b>.

