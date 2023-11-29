---
UID: NF:dxcapi.IDxcContainerBuilder.RemovePart
tech.root: direct3dhlsl
title: IDxcContainerBuilder::RemovePart
ms.date: 04/05/2023
targetos: Windows
description: Remove a part from the container.
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
 - IDxcContainerBuilder::RemovePart
f1_keywords:
 - IDxcContainerBuilder::RemovePart
 - dxcapi/IDxcContainerBuilder::RemovePart
dev_langs:
 - c++
helpviewer_keywords:
 - RemovePart
---

## -description

Remove a part from the container.

## -parameters

### -param fourCC

The identifier of the part to remove; for example, **DXC_PART_PDB**.

## -returns

**S_OK** on success, or **DXC_E_MISSING_PART** if the part wasn't found, or other standard **HRESULT** error code.

## -remarks

## -see-also
