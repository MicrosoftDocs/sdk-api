---
UID: NN:d3d11.ID3D11Device
title: ID3D11Device (d3d11.h)
description: The device interface represents a virtual adapter; it is used to create resources.
helpviewer_keywords: ["ID3D11Device","ID3D11Device interface [Direct3D 11]","ID3D11Device interface [Direct3D 11]","described","b37b606f-bf79-e387-57c4-bebf1cf88722","d3d11/ID3D11Device","direct3d11.id3d11device"]
old-location: direct3d11\id3d11device.htm
tech.root: direct3d11
ms.assetid: 2f2559d9-1cd6-44f6-90e2-ee0f86e39f78
ms.date: 12/05/2018
ms.keywords: ID3D11Device, ID3D11Device interface [Direct3D 11], ID3D11Device interface [Direct3D 11],described, b37b606f-bf79-e387-57c4-bebf1cf88722, d3d11/ID3D11Device, direct3d11.id3d11device
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11Device
 - d3d11/ID3D11Device
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
 - ID3D11Device
---

# ID3D11Device interface


## -description

The device interface represents a virtual adapter; it is used to create resources.
<div class="alert"><b>Note</b>  The latest version of this interface is <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5">ID3D11Device5</a> introduced in the Windows 10 Creators Update. Applications targetting Windows 10 Creators Update should use the <b>ID3D11Device5</b> interface instead of <b>ID3D11Device</b>.</div><div> </div>

## -inheritance

The <b>ID3D11Device</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11Device</b> also has these types of members:

## -remarks

A device is created using <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
