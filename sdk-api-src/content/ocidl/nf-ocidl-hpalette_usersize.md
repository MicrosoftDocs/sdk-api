---
UID: NF:ocidl.HPALETTE_UserSize
tech.root: com
title: HPALETTE_UserSize
ms.date: 02/23/2023
targetos: Windows
description: Calculates the wire size of the HPALETTE object and gets its handle and data. (HPALETTE_UserSize)
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: ole32.dll
req.header: ocidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-marshal-l1-1-0.dll
 - ole32.dll
api_name:
 - HPALETTE_UserSize
f1_keywords:
 - HPALETTE_UserSize
 - ocidl/HPALETTE_UserSize
dev_langs:
 - c++
helpviewer_keywords:
 - HPALETTE_UserSize
---

## -description

Calculates the wire size of the HPALETTE object and gets its handle and data. (HPALETTE_UserSize)

## -parameters

### -param unnamedParam1

The data used by RPC.

### -param unnamedParam2

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the HPALETTE object to be properly aligned when it will be marshaled to the buffer.

### -param unnamedParam3

The object.

## -returns

A LONG value expressing the size of the object.

## -remarks

## -see-also

