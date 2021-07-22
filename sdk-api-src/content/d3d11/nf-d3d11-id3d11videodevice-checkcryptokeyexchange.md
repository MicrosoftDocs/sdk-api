---
UID: NF:d3d11.ID3D11VideoDevice.CheckCryptoKeyExchange
title: ID3D11VideoDevice::CheckCryptoKeyExchange (d3d11.h)
description: Gets a cryptographic key-exchange mechanism that is supported by the driver.
helpviewer_keywords: ["CheckCryptoKeyExchange","CheckCryptoKeyExchange method [Media Foundation]","CheckCryptoKeyExchange method [Media Foundation]","ID3D11VideoDevice interface","D3D11_CRYPTO_TYPE_AES128_CTR","ID3D11VideoDevice interface [Media Foundation]","CheckCryptoKeyExchange method","ID3D11VideoDevice.CheckCryptoKeyExchange","ID3D11VideoDevice::CheckCryptoKeyExchange","d3d11/ID3D11VideoDevice::CheckCryptoKeyExchange","mf.id3d11videodevice_checkcryptokeyexchange"]
old-location: mf\id3d11videodevice_checkcryptokeyexchange.htm
tech.root: mf
ms.assetid: AE2DA6F9-6153-43AF-8E61-26FB9DD5A1D1
ms.date: 12/05/2018
ms.keywords: CheckCryptoKeyExchange, CheckCryptoKeyExchange method [Media Foundation], CheckCryptoKeyExchange method [Media Foundation],ID3D11VideoDevice interface, D3D11_CRYPTO_TYPE_AES128_CTR, ID3D11VideoDevice interface [Media Foundation],CheckCryptoKeyExchange method, ID3D11VideoDevice.CheckCryptoKeyExchange, ID3D11VideoDevice::CheckCryptoKeyExchange, d3d11/ID3D11VideoDevice::CheckCryptoKeyExchange, mf.id3d11videodevice_checkcryptokeyexchange
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
 - ID3D11VideoDevice::CheckCryptoKeyExchange
 - d3d11/ID3D11VideoDevice::CheckCryptoKeyExchange
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
 - ID3D11VideoDevice.CheckCryptoKeyExchange
---

# ID3D11VideoDevice::CheckCryptoKeyExchange


## -description

Gets a cryptographic key-exchange mechanism that is supported by the driver.

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

### -param pDecoderProfile [in]

A pointer to a GUID that specifies the decoding profile. To get  profiles that the driver supports, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile">ID3D11VideoDevice::GetVideoDecoderProfile</a>. If decoding will not be used, set this parameter to <b>NULL</b>.

### -param Index [in]

The zero-based index of the key-exchange type. The driver reports the number of types in the <b>KeyExchangeTypeCount</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps">D3D11_VIDEO_CONTENT_PROTECTION_CAPS</a> structure.

### -param pKeyExchangeType [out]

Receives a GUID that identifies the type of key exchange.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>