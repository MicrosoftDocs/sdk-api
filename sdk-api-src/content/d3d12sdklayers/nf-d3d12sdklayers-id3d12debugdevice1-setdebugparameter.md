---
UID: NF:d3d12sdklayers.ID3D12DebugDevice1.SetDebugParameter
title: ID3D12DebugDevice1::SetDebugParameter (d3d12sdklayers.h)
description: Modifies the D3D12 optional device-wide Debug Layer settings.
helpviewer_keywords: ["ID3D12DebugDevice1 interface","SetDebugParameter method","ID3D12DebugDevice1.SetDebugParameter","ID3D12DebugDevice1::SetDebugParameter","SetDebugParameter","SetDebugParameter method","SetDebugParameter method","ID3D12DebugDevice1 interface","d3d12sdklayers/ID3D12DebugDevice1::SetDebugParameter","direct3d12.id3d12debugdevice1_setdebugparameter"]
old-location: direct3d12\id3d12debugdevice1_setdebugparameter.htm
tech.root: direct3d12
ms.assetid: D97086C6-CED8-4C4E-ADA1-7A172B3202F3
ms.date: 12/05/2018
ms.keywords: ID3D12DebugDevice1 interface,SetDebugParameter method, ID3D12DebugDevice1.SetDebugParameter, ID3D12DebugDevice1::SetDebugParameter, SetDebugParameter, SetDebugParameter method, SetDebugParameter method,ID3D12DebugDevice1 interface, d3d12sdklayers/ID3D12DebugDevice1::SetDebugParameter, direct3d12.id3d12debugdevice1_setdebugparameter
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
 - ID3D12DebugDevice1::SetDebugParameter
 - d3d12sdklayers/ID3D12DebugDevice1::SetDebugParameter
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
 - ID3D12DebugDevice1.SetDebugParameter
---

# ID3D12DebugDevice1::SetDebugParameter


## -description

Modifies the D3D12 optional device-wide Debug Layer settings.

## -parameters

### -param Type

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type">D3D12_DEBUG_DEVICE_PARAMETER_TYPE</a></b>

Specifies a <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type">D3D12_DEBUG_DEVICE_PARAMETER_TYPE</a> value that indicates which debug parameter data to get.

### -param pData [in]

Type: <b>const void*</b>

Debug parameter data to set.

### -param DataSize

Type: <b>UINT</b>

Size in bytes of the data pointed to by <i>pData</i>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter">GetDebugParameter</a>



<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1">ID3D12DebugDevice1</a>