---
UID: NF:d3d10.ID3D10Device.GetCreationFlags
title: ID3D10Device::GetCreationFlags (d3d10.h)
description: Get the flags used during the call to create the device with D3D10CreateDevice.
helpviewer_keywords: ["4822c55e-f89a-b10d-ccba-aa989735a00f","GetCreationFlags","GetCreationFlags method [Direct3D 10]","GetCreationFlags method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","GetCreationFlags method","ID3D10Device.GetCreationFlags","ID3D10Device::GetCreationFlags","d3d10/ID3D10Device::GetCreationFlags","direct3d10.id3d10device_getcreationflags"]
old-location: direct3d10\id3d10device_getcreationflags.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_getcreationflags.htm
ms.date: 12/05/2018
ms.keywords: 4822c55e-f89a-b10d-ccba-aa989735a00f, GetCreationFlags, GetCreationFlags method [Direct3D 10], GetCreationFlags method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GetCreationFlags method, ID3D10Device.GetCreationFlags, ID3D10Device::GetCreationFlags, d3d10/ID3D10Device::GetCreationFlags, direct3d10.id3d10device_getcreationflags
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::GetCreationFlags
 - d3d10/ID3D10Device::GetCreationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.GetCreationFlags
---

# ID3D10Device::GetCreationFlags


## -description

Get the flags used during the call to create the device with <a href="/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice">D3D10CreateDevice</a>.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A bitfield containing the flags used to create the device. See <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag">D3D10_CREATE_DEVICE_FLAG</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
