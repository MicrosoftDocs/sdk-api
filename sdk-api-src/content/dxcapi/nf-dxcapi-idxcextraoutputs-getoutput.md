---
UID: NF:dxcapi.IDxcExtraOutputs.GetOutput
tech.root: direct3dhlsl
title: IDxcExtraOutputs::GetOutput
ms.date: 04/05/2023
targetos: Windows
description: Retrieves the specified output.
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
 - IDxcExtraOutputs::GetOutput
f1_keywords:
 - IDxcExtraOutputs::GetOutput
 - dxcapi/IDxcExtraOutputs::GetOutput
dev_langs:
 - c++
helpviewer_keywords:
 - GetOutput
---

## -description

Retrieves the specified output.

## -parameters

### -param uIndex

The index of the output to retrieve

### -param iid

The interface ID of the output interface.

### -param ppvObject

The optiopnal address of the pointer that receives a pointer to the output, if there is one.

### -param ppOutputType

The optional address of the pointer to receive the output type name blob, if there is one.

### -param ppOutputName

The optional address of a pointer to receive the output name blob, if there is one.

## -returns

The specified output.

## -remarks

## -see-also
