---
UID: NF:d3d12sdklayers.ID3D12DebugCommandList.SetFeatureMask
title: ID3D12DebugCommandList::SetFeatureMask (d3d12sdklayers.h)
description: Turns the debug features for a command list on or off.
helpviewer_keywords: ["ID3D12DebugCommandList interface","SetFeatureMask method","ID3D12DebugCommandList.SetFeatureMask","ID3D12DebugCommandList::SetFeatureMask","SetFeatureMask","SetFeatureMask method","SetFeatureMask method","ID3D12DebugCommandList interface","d3d12sdklayers/ID3D12DebugCommandList::SetFeatureMask","direct3d12.id3d12debugcommandlist_setfeaturemask"]
old-location: direct3d12\id3d12debugcommandlist_setfeaturemask.htm
tech.root: direct3d12
ms.assetid: D2273A6C-7401-44D6-A0E3-F3F2C5DBCB8B
ms.date: 12/05/2018
ms.keywords: ID3D12DebugCommandList interface,SetFeatureMask method, ID3D12DebugCommandList.SetFeatureMask, ID3D12DebugCommandList::SetFeatureMask, SetFeatureMask, SetFeatureMask method, SetFeatureMask method,ID3D12DebugCommandList interface, d3d12sdklayers/ID3D12DebugCommandList::SetFeatureMask, direct3d12.id3d12debugcommandlist_setfeaturemask
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
 - ID3D12DebugCommandList::SetFeatureMask
 - d3d12sdklayers/ID3D12DebugCommandList::SetFeatureMask
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
 - ID3D12DebugCommandList.SetFeatureMask
---

# ID3D12DebugCommandList::SetFeatureMask


## -description

Turns the debug features for a command list on or off.

## -parameters

### -param Mask

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature">D3D12_DEBUG_FEATURE</a></b>

A combination of feature-mask flags that are combined by using a bitwise OR operation. If a flag is present, that feature will be set to on, otherwise the feature will be set to off.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist">ID3D12DebugCommandList</a>