---
UID: NF:d3d10sdklayers.ID3D10SwitchToRef.SetUseRef
title: ID3D10SwitchToRef::SetUseRef (d3d10sdklayers.h)
description: Switch between a hardware and a software device.
helpviewer_keywords: ["7960e1b8-7255-59bd-3f8f-533b12811a49","ID3D10SwitchToRef interface [Direct3D 10]","SetUseRef method","ID3D10SwitchToRef.SetUseRef","ID3D10SwitchToRef::SetUseRef","SetUseRef","SetUseRef method [Direct3D 10]","SetUseRef method [Direct3D 10]","ID3D10SwitchToRef interface","d3d10sdklayers/ID3D10SwitchToRef::SetUseRef","direct3d10.id3d10switchtoref_setuseref"]
old-location: direct3d10\id3d10switchtoref_setuseref.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10switchtoref_setuseref.htm
ms.date: 12/05/2018
ms.keywords: 7960e1b8-7255-59bd-3f8f-533b12811a49, ID3D10SwitchToRef interface [Direct3D 10],SetUseRef method, ID3D10SwitchToRef.SetUseRef, ID3D10SwitchToRef::SetUseRef, SetUseRef, SetUseRef method [Direct3D 10], SetUseRef method [Direct3D 10],ID3D10SwitchToRef interface, d3d10sdklayers/ID3D10SwitchToRef::SetUseRef, direct3d10.id3d10switchtoref_setuseref
req.header: d3d10sdklayers.h
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
 - ID3D10SwitchToRef::SetUseRef
 - d3d10sdklayers/ID3D10SwitchToRef::SetUseRef
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10SwitchToRef.SetUseRef
---

# ID3D10SwitchToRef::SetUseRef


## -description

Switch between a hardware and a software device.

## -parameters

### -param UseRef [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A boolean value. Set this to <b>TRUE</b> to change to a software device, set this to <b>FALSE</b> to change to a hardware device.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

The previous value of <i>UseRef</i>.

## -remarks

This API will fail if the device is not switchable; you must have created a device that is switchable by specifying the D3D10_CREATE_DEVICE_SWITCH_TO_REF flag during device creation (when calling <a href="/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice">D3D10CreateDevice</a>).

Switching from a software device to a hardware device clears all cached objects from system memory. Switching from a hardware device to a software device causes resources to be downloaded to system memory.

## -see-also

<a href="/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice">D3D10CreateDevice</a>



<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10switchtoref">ID3D10SwitchToRef Interface</a>