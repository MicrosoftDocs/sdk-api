---
UID: NF:d3d11.ID3D11VideoDevice.CheckVideoDecoderFormat
title: ID3D11VideoDevice::CheckVideoDecoderFormat (d3d11.h)
description: Given aprofile, checks whether the driver supports a specified output format.
helpviewer_keywords: ["CheckVideoDecoderFormat","CheckVideoDecoderFormat method [Media Foundation]","CheckVideoDecoderFormat method [Media Foundation]","ID3D11VideoDevice interface","ID3D11VideoDevice interface [Media Foundation]","CheckVideoDecoderFormat method","ID3D11VideoDevice.CheckVideoDecoderFormat","ID3D11VideoDevice::CheckVideoDecoderFormat","d3d11/ID3D11VideoDevice::CheckVideoDecoderFormat","mf.id3d11videodevice_checkvideodecoderformat"]
old-location: mf\id3d11videodevice_checkvideodecoderformat.htm
tech.root: mf
ms.assetid: E834DF38-2847-4864-9CFE-A25CAE51C78F
ms.date: 12/05/2018
ms.keywords: CheckVideoDecoderFormat, CheckVideoDecoderFormat method [Media Foundation], CheckVideoDecoderFormat method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CheckVideoDecoderFormat method, ID3D11VideoDevice.CheckVideoDecoderFormat, ID3D11VideoDevice::CheckVideoDecoderFormat, d3d11/ID3D11VideoDevice::CheckVideoDecoderFormat, mf.id3d11videodevice_checkvideodecoderformat
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
 - ID3D11VideoDevice::CheckVideoDecoderFormat
 - d3d11/ID3D11VideoDevice::CheckVideoDecoderFormat
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
 - ID3D11VideoDevice.CheckVideoDecoderFormat
---

# ID3D11VideoDevice::CheckVideoDecoderFormat


## -description

Given aprofile, checks whether the driver supports a specified output format.

## -parameters

### -param pDecoderProfile [in]

A pointer to a GUID that identifies the profile. To get the list of supported profiles, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile">ID3D11VideoDevice::GetVideoDecoderProfile</a>.

### -param Format [in]

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> value that specifies the output format. Typical values include <b>DXGI_FORMAT_NV12</b> and <b>DXGI_FORMAT_420_OPAQUE</b>.

### -param pSupported [out]

Receives the value <b>TRUE</b> if the format is supported, or <b>FALSE</b> otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the driver does not support the profile given in <i>pDecoderProfile</i>, the method returns <b>E_INVALIDARG</b>. If the driver supports the profile, but the DXGI format is not compatible with the profile, the method succeeds but returns the value <b>FALSE</b> in <i>pSupported</i>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>