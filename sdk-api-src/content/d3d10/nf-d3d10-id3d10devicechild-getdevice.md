---
UID: NF:d3d10.ID3D10DeviceChild.GetDevice
title: ID3D10DeviceChild::GetDevice (d3d10.h)
description: Get a pointer to the device that created this interface. (ID3D10DeviceChild.GetDevice)
helpviewer_keywords: ["GetDevice","GetDevice method [Direct3D 10]","GetDevice method [Direct3D 10]","ID3D10DeviceChild interface","ID3D10DeviceChild interface [Direct3D 10]","GetDevice method","ID3D10DeviceChild.GetDevice","ID3D10DeviceChild::GetDevice","a6448c63-5b6c-87fa-33e0-73a8850ca573","d3d10/ID3D10DeviceChild::GetDevice","direct3d10.id3d10devicechild_getdevice"]
old-location: direct3d10\id3d10devicechild_getdevice.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10devicechild_getdevice.htm
ms.date: 12/05/2018
ms.keywords: GetDevice, GetDevice method [Direct3D 10], GetDevice method [Direct3D 10],ID3D10DeviceChild interface, ID3D10DeviceChild interface [Direct3D 10],GetDevice method, ID3D10DeviceChild.GetDevice, ID3D10DeviceChild::GetDevice, a6448c63-5b6c-87fa-33e0-73a8850ca573, d3d10/ID3D10DeviceChild::GetDevice, direct3d10.id3d10devicechild_getdevice
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
 - ID3D10DeviceChild::GetDevice
 - d3d10/ID3D10DeviceChild::GetDevice
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
 - ID3D10DeviceChild.GetDevice
---

# ID3D10DeviceChild::GetDevice


## -description

Get a pointer to the device that created this interface.

## -parameters

### -param ppDevice [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>**</b>

Address of a pointer to a device (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>).

## -remarks

Any returned interfaces will have their reference count incremented by one, so be sure to call ::release() on the returned pointer(s) before they are freed or else you will have a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild Interface</a>
