---
UID: NF:d3d11.ID3D11DeviceChild.GetDevice
title: ID3D11DeviceChild::GetDevice (d3d11.h)
description: Get a pointer to the device that created this interface. (ID3D11DeviceChild.GetDevice)
helpviewer_keywords: ["07aa3147-aab3-5e52-2809-7bddfdb31126","GetDevice","GetDevice method [Direct3D 11]","GetDevice method [Direct3D 11]","ID3D11DeviceChild interface","ID3D11DeviceChild interface [Direct3D 11]","GetDevice method","ID3D11DeviceChild.GetDevice","ID3D11DeviceChild::GetDevice","d3d11/ID3D11DeviceChild::GetDevice","direct3d11.id3d11devicechild_getdevice"]
old-location: direct3d11\id3d11devicechild_getdevice.htm
tech.root: direct3d11
ms.assetid: d18f43ef-4edc-47ff-b1be-1be670c2ccb2
ms.date: 12/05/2018
ms.keywords: 07aa3147-aab3-5e52-2809-7bddfdb31126, GetDevice, GetDevice method [Direct3D 11], GetDevice method [Direct3D 11],ID3D11DeviceChild interface, ID3D11DeviceChild interface [Direct3D 11],GetDevice method, ID3D11DeviceChild.GetDevice, ID3D11DeviceChild::GetDevice, d3d11/ID3D11DeviceChild::GetDevice, direct3d11.id3d11devicechild_getdevice
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
 - ID3D11DeviceChild::GetDevice
 - d3d11/ID3D11DeviceChild::GetDevice
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
 - ID3D11DeviceChild.GetDevice
---

# ID3D11DeviceChild::GetDevice


## -description

Get a pointer to the device that created this interface.

## -parameters

### -param ppDevice [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>**</b>

Address of a pointer to a device (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>).

## -remarks

Any returned interfaces will have their reference count incremented by one, so be sure to call ::release() on the returned pointer(s) before they are freed or else you will have a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
