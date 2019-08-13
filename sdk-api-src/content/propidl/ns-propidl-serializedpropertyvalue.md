---
UID: NS:propidl.tagSERIALIZEDPROPERTYVALUE
title: SERIALIZEDPROPERTYVALUE (propidl.h)
author: windows-sdk-content
description: A range of memory of arbitrary type that represents a serialized PROPVARIANT structure.
old-location: shell\SERIALIZEDPROPERTYVALUE.htm
tech.root: shell
ms.assetid: ab64a16e-624d-427a-8f9c-5c8c4a9df625
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SERIALIZEDPROPERTYVALUE, SERIALIZEDPROPERTYVALUE structure [Windows Shell], _shell_SERIALIZEDPROPERTYVALUE, propidl/SERIALIZEDPROPERTYVALUE, shell.SERIALIZEDPROPERTYVALUE
ms.topic: struct
f1_keywords: 
 - "propidl/SERIALIZEDPROPERTYVALUE"
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
ms.custom: 19H1
---

# SERIALIZEDPROPERTYVALUE structure


## -description


A range of memory of arbitrary type that represents a serialized <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. Programs should not inspect the contents of a <b>SERIALIZEDPROPERTYVALUE</b>; instead, they should manipulate it with the <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant">StgSerializePropVariant</a> and <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant">StgDeserializePropVariant</a> functions.


## -struct-fields




### -field dwType

Type: <b>DWORD</b>

Encodes type information about the serialized <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. Programs should not inspect this member directly; instead, they should use the <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant">StgDeserializePropVariant</a> function and inspect the <b>vt</b>  member of the resulting <b>PROPVARIANT</b> structure.


### -field rgb

Type: <b>BYTE[1]</b>

A variable-length additional data that depends on the type passed in <b>dwType</b>.

