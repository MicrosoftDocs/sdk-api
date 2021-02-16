---
UID: NF:d3d12sdklayers.ID3D12DebugDevice1.GetDebugParameter
title: ID3D12DebugDevice1::GetDebugParameter (d3d12sdklayers.h)
description: Gets optional device-wide Debug Layer settings.
helpviewer_keywords: ["GetDebugParameter","GetDebugParameter method","GetDebugParameter method","ID3D12DebugDevice1 interface","ID3D12DebugDevice1 interface","GetDebugParameter method","ID3D12DebugDevice1.GetDebugParameter","ID3D12DebugDevice1::GetDebugParameter","d3d12sdklayers/ID3D12DebugDevice1::GetDebugParameter","direct3d12.id3d12debugdevice1_getdebugparameter"]
old-location: direct3d12\id3d12debugdevice1_getdebugparameter.htm
tech.root: direct3d12
ms.assetid: 13A7E7D6-FF00-4E17-A7C5-C383F93F6A06
ms.date: 12/05/2018
ms.keywords: GetDebugParameter, GetDebugParameter method, GetDebugParameter method,ID3D12DebugDevice1 interface, ID3D12DebugDevice1 interface,GetDebugParameter method, ID3D12DebugDevice1.GetDebugParameter, ID3D12DebugDevice1::GetDebugParameter, d3d12sdklayers/ID3D12DebugDevice1::GetDebugParameter, direct3d12.id3d12debugdevice1_getdebugparameter
req.header: d3d12sdklayers.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12DebugDevice1::GetDebugParameter
 - d3d12sdklayers/ID3D12DebugDevice1::GetDebugParameter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugDevice1.GetDebugParameter
---

# ID3D12DebugDevice1::GetDebugParameter


## -description

Gets optional device-wide Debug Layer settings.

## -parameters

### -param Type

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type">D3D12_DEBUG_DEVICE_PARAMETER_TYPE</a></b>

Specifies a <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type">D3D12_DEBUG_DEVICE_PARAMETER_TYPE</a> value that indicates which debug parameter data to set.

### -param pData [out]

Type: <b>void*</b>

Points to the memory that will be filled with a copy of the debug parameter data. The interpretation of this data depends on the <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type">D3D12_DEBUG_DEVICE_PARAMETER_TYPE</a> given in the <i>Type</i> parameter.

### -param DataSize

Type: <b>UINT</b>

Size in bytes of the memory buffer pointed to by <i>pData</i>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1">ID3D12DebugDevice1</a>



<a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter">SetDebugParameter</a>