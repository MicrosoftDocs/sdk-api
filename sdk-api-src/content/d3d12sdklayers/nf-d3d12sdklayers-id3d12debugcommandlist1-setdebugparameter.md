---
UID: NF:d3d12sdklayers.ID3D12DebugCommandList1.SetDebugParameter
title: ID3D12DebugCommandList1::SetDebugParameter (d3d12sdklayers.h)
description: Modifies optional Debug Layer settings of a command list.
helpviewer_keywords: ["ID3D12DebugCommandList1 interface","SetDebugParameter method","ID3D12DebugCommandList1.SetDebugParameter","ID3D12DebugCommandList1::SetDebugParameter","SetDebugParameter","SetDebugParameter method","SetDebugParameter method","ID3D12DebugCommandList1 interface","d3d12sdklayers/ID3D12DebugCommandList1::SetDebugParameter","direct3d12.id3d12debugcommandlist1_setdebugparameter"]
old-location: direct3d12\id3d12debugcommandlist1_setdebugparameter.htm
tech.root: direct3d12
ms.assetid: 8D93895A-BED7-4A86-893B-ACB5FA1B160F
ms.date: 12/05/2018
ms.keywords: ID3D12DebugCommandList1 interface,SetDebugParameter method, ID3D12DebugCommandList1.SetDebugParameter, ID3D12DebugCommandList1::SetDebugParameter, SetDebugParameter, SetDebugParameter method, SetDebugParameter method,ID3D12DebugCommandList1 interface, d3d12sdklayers/ID3D12DebugCommandList1::SetDebugParameter, direct3d12.id3d12debugcommandlist1_setdebugparameter
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
 - ID3D12DebugCommandList1::SetDebugParameter
 - d3d12sdklayers/ID3D12DebugCommandList1::SetDebugParameter
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
 - ID3D12DebugCommandList1.SetDebugParameter
---

# ID3D12DebugCommandList1::SetDebugParameter


## -description

Modifies optional Debug Layer settings of a command list.

## -parameters

### -param Type

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a></b>

Specifies a <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a> value that indicates which debug parameter data to set.

### -param pData [in]

Type: <b>const void*</b>

Pointer to debug parameter data to set.  The interpretation of this data depends on the <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a> given in the <i>Type</i> parameter.

### -param DataSize

Type: <b>UINT</b>

Specifies the size in bytes of the debug parameter <i>pData</i>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

Certain debug behaviors of D3D12 Debug Layer can be modified by setting debug parameters.  These can be used to toggle extra validation or expose experimental debug features.

<b>ID3D12DebugCommandList1::SetDebugParameter</b> only impacts debug settings for the associated command list.  For device-wide debug parameters see the <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter">ID3D12DebugDevice1::SetDebugParameter</a> method.

Resetting a command list restores the debug parameters to the default values.  This is because a command list reset is treated as equivalent to creating a new command list.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter">GetDebugParameter</a>



<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1">ID3D12DebugCommandList1</a>