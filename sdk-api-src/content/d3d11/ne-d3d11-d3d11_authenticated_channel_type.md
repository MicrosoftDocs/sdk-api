---
UID: NE:d3d11.D3D11_AUTHENTICATED_CHANNEL_TYPE
title: D3D11_AUTHENTICATED_CHANNEL_TYPE (d3d11.h)
description: Specifies the type of Microsoft Direct3D authenticated channel.
helpviewer_keywords: ["D3D11_AUTHENTICATED_CHANNEL_D3D11","D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE","D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE","D3D11_AUTHENTICATED_CHANNEL_TYPE","D3D11_AUTHENTICATED_CHANNEL_TYPE enumeration [Media Foundation]","d3d11/D3D11_AUTHENTICATED_CHANNEL_D3D11","d3d11/D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE","d3d11/D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE","d3d11/D3D11_AUTHENTICATED_CHANNEL_TYPE","mf.d3d11_authenticated_channel_type"]
old-location: mf\d3d11_authenticated_channel_type.htm
tech.root: mf
ms.assetid: 4B4E8AA9-5FFE-4ADB-AC83-89FE1BCE27EB
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_CHANNEL_D3D11, D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE, D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE, D3D11_AUTHENTICATED_CHANNEL_TYPE, D3D11_AUTHENTICATED_CHANNEL_TYPE enumeration [Media Foundation], d3d11/D3D11_AUTHENTICATED_CHANNEL_D3D11, d3d11/D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE, d3d11/D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE, d3d11/D3D11_AUTHENTICATED_CHANNEL_TYPE, mf.d3d11_authenticated_channel_type
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: D3D11_AUTHENTICATED_CHANNEL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_CHANNEL_TYPE
 - d3d11/D3D11_AUTHENTICATED_CHANNEL_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_AUTHENTICATED_CHANNEL_TYPE
---

# D3D11_AUTHENTICATED_CHANNEL_TYPE enumeration


## -description

Specifies the type of Microsoft Direct3D authenticated channel.

## -enum-fields

### -field D3D11_AUTHENTICATED_CHANNEL_D3D11:1

Direct3D 11 channel. This channel provides communication with the Direct3D runtime.

### -field D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE:2

Software driver channel. This channel provides communication with a driver that implements content protection mechanisms in software.

### -field D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE:3

Hardware driver channel. This channel provides communication with a driver that implements content protection mechanisms in the GPU hardware.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
