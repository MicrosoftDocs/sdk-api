---
UID: NF:d3d11.ID3D11Device.GetImmediateContext
title: ID3D11Device::GetImmediateContext (d3d11.h)
description: Gets an immediate context, which can play back command lists. (ID3D11Device.GetImmediateContext)
helpviewer_keywords: ["2f9e01b9-f7a8-4cdb-2811-bbd0a44df05f","GetImmediateContext","GetImmediateContext method [Direct3D 11]","GetImmediateContext method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","GetImmediateContext method","ID3D11Device.GetImmediateContext","ID3D11Device::GetImmediateContext","d3d11/ID3D11Device::GetImmediateContext","direct3d11.id3d11device_getimmediatecontext"]
old-location: direct3d11\id3d11device_getimmediatecontext.htm
tech.root: direct3d11
ms.assetid: 0349f0b8-7696-4d72-bed4-d39b9ac90f6c
ms.date: 12/05/2018
ms.keywords: 2f9e01b9-f7a8-4cdb-2811-bbd0a44df05f, GetImmediateContext, GetImmediateContext method [Direct3D 11], GetImmediateContext method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],GetImmediateContext method, ID3D11Device.GetImmediateContext, ID3D11Device::GetImmediateContext, d3d11/ID3D11Device::GetImmediateContext, direct3d11.id3d11device_getimmediatecontext
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
 - ID3D11Device::GetImmediateContext
 - d3d11/ID3D11Device::GetImmediateContext
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
 - ID3D11Device.GetImmediateContext
---

# ID3D11Device::GetImmediateContext


## -description

Gets an immediate context, which can play back command lists.

## -parameters

### -param ppImmediateContext [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>**</b>

Upon completion of the method, the passed pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> interface pointer is initialized.

## -remarks

The <b>GetImmediateContext</b> method returns an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> object that represents an immediate context which is used to perform rendering that you want immediately submitted to a device. For most applications, an immediate context is the primary object that is used to draw your scene.

The <b>GetImmediateContext</b> method increments the reference count of the immediate context by one. Therefore, you must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the returned interface pointer when you are done with it to avoid a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
