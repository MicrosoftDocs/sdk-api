---
UID: NF:d3d11.ID3D11VideoDevice.CreateCryptoSession
title: ID3D11VideoDevice::CreateCryptoSession (d3d11.h)
description: Creates a cryptographic session to encrypt video content that is sent to the graphics driver.
helpviewer_keywords: ["CreateCryptoSession","CreateCryptoSession method [Media Foundation]","CreateCryptoSession method [Media Foundation]","ID3D11VideoDevice interface","D3D11_CRYPTO_TYPE_AES128_CTR","D3D11_KEY_EXCHANGE_RSAES_OAEP","ID3D11VideoDevice interface [Media Foundation]","CreateCryptoSession method","ID3D11VideoDevice.CreateCryptoSession","ID3D11VideoDevice::CreateCryptoSession","d3d11/ID3D11VideoDevice::CreateCryptoSession","mf.id3d11videodevice_createcryptosession"]
old-location: mf\id3d11videodevice_createcryptosession.htm
tech.root: mf
ms.assetid: 384EE3E1-2B62-477B-8A3F-FDCD06959B74
ms.date: 12/05/2018
ms.keywords: CreateCryptoSession, CreateCryptoSession method [Media Foundation], CreateCryptoSession method [Media Foundation],ID3D11VideoDevice interface, D3D11_CRYPTO_TYPE_AES128_CTR, D3D11_KEY_EXCHANGE_RSAES_OAEP, ID3D11VideoDevice interface [Media Foundation],CreateCryptoSession method, ID3D11VideoDevice.CreateCryptoSession, ID3D11VideoDevice::CreateCryptoSession, d3d11/ID3D11VideoDevice::CreateCryptoSession, mf.id3d11videodevice_createcryptosession
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
 - ID3D11VideoDevice::CreateCryptoSession
 - d3d11/ID3D11VideoDevice::CreateCryptoSession
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
 - ID3D11VideoDevice.CreateCryptoSession
---

# ID3D11VideoDevice::CreateCryptoSession


## -description

Creates a cryptographic session to encrypt video content that is sent to the graphics driver.

## -parameters

### -param pCryptoType [in]

A pointer to a GUID that specifies the type of encryption to use. The following GUIDs are defined.



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

A pointer to a GUID that specifies the decoding profile. For a list of possible values, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile">ID3D11VideoDevice::GetVideoDecoderProfile</a>. If decoding will not be used, set this parameter to <b>NULL</b>.

### -param pKeyExchangeType [in]

A pointer to a GUID that specifies the type of key exchange.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="D3D11_KEY_EXCHANGE_RSAES_OAEP"></a><a id="d3d11_key_exchange_rsaes_oaep"></a><dl>
<dt><b>D3D11_KEY_EXCHANGE_RSAES_OAEP</b></dt>
</dl>
</td>
<td width="60%">
The caller will create the session key, encrypt it with RSA Encryption Scheme - Optimal Asymmetric Encryption Padding (RSAES-OAEP) by using the driver's public key, and pass the session key to the driver.

</td>
</tr>
</table>

### -param ppCryptoSession [out]

Receives a pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate">ID3D11DeviceContext::ClearState</a> method does not affect the internal state of the cryptographic session.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>