---
UID: NF:dxcapi.IDxcUtils.GetDxilContainerPart
tech.root: direct3dhlsl
title: IDxcUtils::GetDxilContainerPart
ms.date: 04/05/2023
targetos: Windows
description: TBD
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
 - IDxcUtils::GetDxilContainerPart
f1_keywords:
 - IDxcUtils::GetDxilContainerPart
 - dxcapi/IDxcUtils::GetDxilContainerPart
dev_langs:
 - c++
helpviewer_keywords:
 - GetDxilContainerPart
---

## -description

Retrieve a single part from a DXIL container.

## -parameters

### -param pShader

The shader to retrieve the part from.

### -param DxcPart

The part to retrieve; for example, **DXC_PART_ROOT_SIGNATURE**.

### -param ppPartData

The address of the pointer that receives a pointer to the part. The returned pointer points inside the buffer passed in *pShader*.

### -param pPartSizeInBytes

The address of the pointer that receives the size of the part.

## -returns

## -remarks

## -see-also
