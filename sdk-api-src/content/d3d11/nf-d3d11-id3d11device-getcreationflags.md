---
UID: NF:d3d11.ID3D11Device.GetCreationFlags
title: ID3D11Device::GetCreationFlags (d3d11.h)
description: Get the flags used during the call to create the device with D3D11CreateDevice.
helpviewer_keywords: ["19c344e0-8664-5c52-5bb8-46d3941967fa","GetCreationFlags","GetCreationFlags method [Direct3D 11]","GetCreationFlags method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","GetCreationFlags method","ID3D11Device.GetCreationFlags","ID3D11Device::GetCreationFlags","d3d11/ID3D11Device::GetCreationFlags","direct3d11.id3d11device_getcreationflags"]
old-location: direct3d11\id3d11device_getcreationflags.htm
tech.root: direct3d11
ms.assetid: 124e1a50-8fae-4af5-8a9f-a56f000ccbe7
ms.date: 12/05/2018
ms.keywords: 19c344e0-8664-5c52-5bb8-46d3941967fa, GetCreationFlags, GetCreationFlags method [Direct3D 11], GetCreationFlags method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],GetCreationFlags method, ID3D11Device.GetCreationFlags, ID3D11Device::GetCreationFlags, d3d11/ID3D11Device::GetCreationFlags, direct3d11.id3d11device_getcreationflags
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::GetCreationFlags
 - d3d11/ID3D11Device::GetCreationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.GetCreationFlags
---

# ID3D11Device::GetCreationFlags


## -description

Get the flags used during the call to create the device with <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a>.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A bitfield containing the flags used to create the device. See <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_FLAG</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
