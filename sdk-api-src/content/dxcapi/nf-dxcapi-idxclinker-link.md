---
UID: NF:dxcapi.IDxcLinker.Link
tech.root: direct3dhlsl
title: IDxcLinker::Link
ms.date: 04/05/2023
targetos: Windows
description: Links the shader, and produces a shader blob that the Direct3D runtime can use.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dxcapi.h
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
 - HeaderDef
api_location:
 - dxcapi.h
api_name:
 - IDxcLinker::Link
f1_keywords:
 - IDxcLinker::Link
 - dxcapi/IDxcLinker::Link
dev_langs:
 - c++
helpviewer_keywords:
 - Link
---

## -description

Links the shader, and produces a shader blob that the Direct3D runtime can use.

## -parameters

### -param pEntryName

Entry point name.

### -param pTargetProfile

Shader profile to link.

### -param pLibNames

An array of library names to link.

### -param libCount

The number of libraries to link.

### -param pArguments

An array of pointers to arguments.

### -param argCount

The number of arguments.

### -param ppResult

The linker output status, buffer, and errors.

## -returns

## -remarks

## -see-also
