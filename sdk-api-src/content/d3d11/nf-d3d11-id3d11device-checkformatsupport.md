---
UID: NF:d3d11.ID3D11Device.CheckFormatSupport
title: ID3D11Device::CheckFormatSupport (d3d11.h)
description: Get the support of a given format on the installed video device. (ID3D11Device.CheckFormatSupport)
helpviewer_keywords: ["2d26cce0-cf41-b6fc-ed00-e69b3d5ba58f","CheckFormatSupport","CheckFormatSupport method [Direct3D 11]","CheckFormatSupport method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CheckFormatSupport method","ID3D11Device.CheckFormatSupport","ID3D11Device::CheckFormatSupport","d3d11/ID3D11Device::CheckFormatSupport","direct3d11.id3d11device_checkformatsupport"]
old-location: direct3d11\id3d11device_checkformatsupport.htm
tech.root: direct3d11
ms.assetid: d5442fe8-e510-4bda-9df0-377b465cdd5e
ms.date: 12/05/2018
ms.keywords: 2d26cce0-cf41-b6fc-ed00-e69b3d5ba58f, CheckFormatSupport, CheckFormatSupport method [Direct3D 11], CheckFormatSupport method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CheckFormatSupport method, ID3D11Device.CheckFormatSupport, ID3D11Device::CheckFormatSupport, d3d11/ID3D11Device::CheckFormatSupport, direct3d11.id3d11device_checkformatsupport
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
 - ID3D11Device::CheckFormatSupport
 - d3d11/ID3D11Device::CheckFormatSupport
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
 - ID3D11Device.CheckFormatSupport
---

# ID3D11Device::CheckFormatSupport


## -description

Get the support of a given format on the installed video device.

## -parameters

### -param Format [in]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> enumeration that describes a format for which to check for support.

### -param pFormatSupport [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A bitfield of <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support">D3D11_FORMAT_SUPPORT</a> enumeration values describing how the specified format is supported on the installed device. 
        The values are ORed together.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns E_INVALIDARG if the <i>Format</i> parameter is <b>NULL</b>, or returns E_FAIL if the 
      described format does not exist.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
