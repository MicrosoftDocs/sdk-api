---
UID: NF:dxcapi.IDxcUtils.CreateReflection
tech.root: direct3dhlsl
title: IDxcUtils::CreateReflection
ms.date: 04/05/2023
targetos: Windows
description: Create a reflection interface from a serialized DXIL container, or the **DXC_PART_REFLECTION_DATA** blob contents.
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
 - IDxcUtils::CreateReflection
f1_keywords:
 - IDxcUtils::CreateReflection
 - dxcapi/IDxcUtils::CreateReflection
dev_langs:
 - c++
helpviewer_keywords:
 - CreateReflection
---

## -description

Create a reflection interface from a serialized DXIL container, or the **DXC_PART_REFLECTION_DATA** blob contents. Use the returned interface with interfaces such as [ID3D12ShaderReflection](/windows/win32/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection).

## -parameters

### -param pData

The source data.

### -param iid

The interface ID of the reflection interface to create.

### -param ppvReflection

The address of the pointer that receives a pointer to the newly-created reflection interface.

## -returns

## -remarks

## -see-also
