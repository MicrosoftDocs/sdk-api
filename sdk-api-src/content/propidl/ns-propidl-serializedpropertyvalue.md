---
UID: NS:propidl.tagSERIALIZEDPROPERTYVALUE
title: SERIALIZEDPROPERTYVALUE
author: windows-sdk-content
description: A range of memory of arbitrary type that represents a serialized PROPVARIANT structure.
old-location: shell\SERIALIZEDPROPERTYVALUE.htm
tech.root: shell
ms.assetid: ab64a16e-624d-427a-8f9c-5c8c4a9df625
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SERIALIZEDPROPERTYVALUE, SERIALIZEDPROPERTYVALUE structure [Windows Shell], _shell_SERIALIZEDPROPERTYVALUE, propidl/SERIALIZEDPROPERTYVALUE, shell.SERIALIZEDPROPERTYVALUE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: propidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propidl.h
api_name:
 - SERIALIZEDPROPERTYVALUE
product: Windows
targetos: Windows
req.typenames: SERIALIZEDPROPERTYVALUE
req.redist: 
---

# SERIALIZEDPROPERTYVALUE structure


## -description


A range of memory of arbitrary type that represents a serialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. Programs should not inspect the contents of a <b>SERIALIZEDPROPERTYVALUE</b>; instead, they should manipulate it with the <a href="https://msdn.microsoft.com/c588e239-616f-4569-88b5-6bfb504cefa1">StgSerializePropVariant</a> and <a href="https://msdn.microsoft.com/0517ef4d-e57c-4613-8d11-5e1eb14eb9fa">StgDeserializePropVariant</a> functions.


## -struct-fields




### -field dwType

Type: <b>DWORD</b>

Encodes type information about the serialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. Programs should not inspect this member directly; instead, they should use the <a href="https://msdn.microsoft.com/0517ef4d-e57c-4613-8d11-5e1eb14eb9fa">StgDeserializePropVariant</a> function and inspect the <b>vt</b>  member of the resulting <b>PROPVARIANT</b> structure.


### -field rgb

Type: <b>BYTE[1]</b>

A variable-length additional data that depends on the type passed in <b>dwType</b>.

