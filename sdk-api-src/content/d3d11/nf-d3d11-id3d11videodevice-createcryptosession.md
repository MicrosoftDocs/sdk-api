---
UID: NF:d3d11.ID3D11VideoDevice.CreateCryptoSession
title: ID3D11VideoDevice::CreateCryptoSession
author: windows-sdk-content
description: Creates a cryptographic session to encrypt video content that is sent to the graphics driver.
old-location: mf\id3d11videodevice_createcryptosession.htm
tech.root: medfound
ms.assetid: 384EE3E1-2B62-477B-8A3F-FDCD06959B74
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateCryptoSession, CreateCryptoSession method [Media Foundation], CreateCryptoSession method [Media Foundation],ID3D11VideoDevice interface, D3D11_CRYPTO_TYPE_AES128_CTR, D3D11_KEY_EXCHANGE_RSAES_OAEP, ID3D11VideoDevice interface [Media Foundation],CreateCryptoSession method, ID3D11VideoDevice.CreateCryptoSession, ID3D11VideoDevice::CreateCryptoSession, d3d11/ID3D11VideoDevice::CreateCryptoSession, mf.id3d11videodevice_createcryptosession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoDevice.CreateCryptoSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

A pointer to a GUID that specifies the decoding profile. For a list of possible values, see <a href="https://msdn.microsoft.com/8D958469-7FC3-4B4F-82BF-271662CF0088">ID3D11VideoDevice::GetVideoDecoderProfile</a>. If decoding will not be used, set this parameter to <b>NULL</b>.




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

Receives a pointer to the <a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/dabf52f5-0f69-4017-863c-9e3ecef4d5dc">ID3D11DeviceContext::ClearState</a> method does not affect the internal state of the cryptographic session.




## -see-also




<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

