---
UID: NF:rometadataresolution.RoCreatePropertySetSerializer
tech.root: WinRT
title: RoCreatePropertySetSerializer
ms.date: 01/17/2025
targetos: Windows
description: Creates a new instance of IPropertySetSerializer.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: WinTypes.dll
req.header: rometadataresolution.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: WindowsApp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2019
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ext-ms-win-ro-typeresolution-l1-1-1.dll
 - api-ms-win-ro-typeresolution-l1-1-1.dll
 - api-ms-win-core-winrt-propertysetprivate-l1-1-1.dll
 - rometadataresolution.h
api_name:
 - RoCreatePropertySetSerializer
f1_keywords:
 - RoCreatePropertySetSerializer
 - rometadataresolution/RoCreatePropertySetSerializer
dev_langs:
 - c++
helpviewer_keywords:
 - RoCreatePropertySetSerializer
---

## -description

Creates a new instance of an object that implements [IPropertySetSerializer](/uwp/api/windows.storage.streams.ipropertysetserializer).

## -parameters

### -param ppPropertySetSerializer

Recieves a pointer to the new instance of **IPropertySetSerializer**.

## -returns

S_OK on success.

## -remarks

The returned **IPropertySetSerializer** can be used to serialize and deserialize property
sets to and from buffers that are used within a process or passed between two running processes.
There is no guarantee that a serialized property set buffer can be deserialized
by another computer or by the same computer after a reboot.

## -see-also

