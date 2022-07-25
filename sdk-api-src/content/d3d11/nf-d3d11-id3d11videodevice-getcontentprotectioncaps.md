---
UID: NF:d3d11.ID3D11VideoDevice.GetContentProtectionCaps
title: ID3D11VideoDevice::GetContentProtectionCaps (d3d11.h)
description: Queries the driver for its content protection capabilities.
helpviewer_keywords: ["D3D11_CRYPTO_TYPE_AES128_CTR","GetContentProtectionCaps","GetContentProtectionCaps method [Media Foundation]","GetContentProtectionCaps method [Media Foundation]","ID3D11VideoDevice interface","ID3D11VideoDevice interface [Media Foundation]","GetContentProtectionCaps method","ID3D11VideoDevice.GetContentProtectionCaps","ID3D11VideoDevice::GetContentProtectionCaps","d3d11/ID3D11VideoDevice::GetContentProtectionCaps","mf.id3d11videodevice_getcontentprotectioncaps"]
old-location: mf\id3d11videodevice_getcontentprotectioncaps.htm
tech.root: mf
ms.assetid: 3BF2D2B9-6A12-4E71-9F52-829BABA32EF6
ms.date: 12/05/2018
ms.keywords: D3D11_CRYPTO_TYPE_AES128_CTR, GetContentProtectionCaps, GetContentProtectionCaps method [Media Foundation], GetContentProtectionCaps method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],GetContentProtectionCaps method, ID3D11VideoDevice.GetContentProtectionCaps, ID3D11VideoDevice::GetContentProtectionCaps, d3d11/ID3D11VideoDevice::GetContentProtectionCaps, mf.id3d11videodevice_getcontentprotectioncaps
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
 - ID3D11VideoDevice::GetContentProtectionCaps
 - d3d11/ID3D11VideoDevice::GetContentProtectionCaps
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
 - ID3D11VideoDevice.GetContentProtectionCaps
---

# ID3D11VideoDevice::GetContentProtectionCaps


## -description

Queries the driver for its content protection capabilities.

## -parameters

### -param pCryptoType [in]

A pointer to a GUID that specifies the type of encryption to be used. The following GUIDs are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="D3D11_CRYPTO_TYPE_AES128_CTR"></a><a id="d3d11_crypto_type_aes128_ctr"></a><dl>
<dt><b>D3D11_CRYPTO_TYPE_AES128_CTR</b></dt>
</dl>
</td>
<td width="60%">
128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher.


</td>
</tr>
</table>
 

If no encryption will be used, set this parameter to <b>NULL</b>.

### -param pDecoderProfile [in]

A pointer to a GUID that specifies the decoding profile. To get profiles that the driver supports, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile">ID3D11VideoDevice::GetVideoDecoderProfile</a>. If decoding will not be used, set this parameter to <b>NULL</b>.

The driver might disallow some combinations of encryption type and profile.

### -param pCaps [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps">D3D11_VIDEO_CONTENT_PROTECTION_CAPS</a> structure. The method fills in this structure with the driver's content protection capabilities.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>