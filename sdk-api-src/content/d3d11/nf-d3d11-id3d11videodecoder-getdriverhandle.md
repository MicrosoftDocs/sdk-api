---
UID: NF:d3d11.ID3D11VideoDecoder.GetDriverHandle
title: ID3D11VideoDecoder::GetDriverHandle (d3d11.h)
description: Gets a handle to the driver.
helpviewer_keywords: ["GetDriverHandle","GetDriverHandle method [Media Foundation]","GetDriverHandle method [Media Foundation]","ID3D11VideoDecoder interface","ID3D11VideoDecoder interface [Media Foundation]","GetDriverHandle method","ID3D11VideoDecoder.GetDriverHandle","ID3D11VideoDecoder::GetDriverHandle","d3d11/ID3D11VideoDecoder::GetDriverHandle","mf.id3d11videodecoder_getdriverhandle"]
old-location: mf\id3d11videodecoder_getdriverhandle.htm
tech.root: mf
ms.assetid: CD9A46DB-C16D-4DF4-972B-2CE8398CEE98
ms.date: 12/05/2018
ms.keywords: GetDriverHandle, GetDriverHandle method [Media Foundation], GetDriverHandle method [Media Foundation],ID3D11VideoDecoder interface, ID3D11VideoDecoder interface [Media Foundation],GetDriverHandle method, ID3D11VideoDecoder.GetDriverHandle, ID3D11VideoDecoder::GetDriverHandle, d3d11/ID3D11VideoDecoder::GetDriverHandle, mf.id3d11videodecoder_getdriverhandle
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoDecoder::GetDriverHandle
 - d3d11/ID3D11VideoDecoder::GetDriverHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoDecoder.GetDriverHandle
---

# ID3D11VideoDecoder::GetDriverHandle


## -description

Gets a handle to the driver.

## -parameters

### -param pDriverHandle [out]

Receives a handle to the driver.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The driver handle can be used to configure content protection.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a>