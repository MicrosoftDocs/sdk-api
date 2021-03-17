---
UID: NF:d3d11.ID3D11CryptoSession.GetCryptoType
title: ID3D11CryptoSession::GetCryptoType (d3d11.h)
description: Gets the type of encryption that is supported by this session.
helpviewer_keywords: ["D3D11_CRYPTO_TYPE_AES128_CTR","GetCryptoType","GetCryptoType method [Media Foundation]","GetCryptoType method [Media Foundation]","ID3D11CryptoSession interface","ID3D11CryptoSession interface [Media Foundation]","GetCryptoType method","ID3D11CryptoSession.GetCryptoType","ID3D11CryptoSession::GetCryptoType","d3d11/ID3D11CryptoSession::GetCryptoType","mf.id3d11cryptosession_getcryptotype"]
old-location: mf\id3d11cryptosession_getcryptotype.htm
tech.root: mf
ms.assetid: D5F62BFA-EA46-4BDD-8D8C-5D9D5BB590B9
ms.date: 12/05/2018
ms.keywords: D3D11_CRYPTO_TYPE_AES128_CTR, GetCryptoType, GetCryptoType method [Media Foundation], GetCryptoType method [Media Foundation],ID3D11CryptoSession interface, ID3D11CryptoSession interface [Media Foundation],GetCryptoType method, ID3D11CryptoSession.GetCryptoType, ID3D11CryptoSession::GetCryptoType, d3d11/ID3D11CryptoSession::GetCryptoType, mf.id3d11cryptosession_getcryptotype
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
 - ID3D11CryptoSession::GetCryptoType
 - d3d11/ID3D11CryptoSession::GetCryptoType
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
 - ID3D11CryptoSession.GetCryptoType
---

# ID3D11CryptoSession::GetCryptoType


## -description

Gets the type of encryption that is supported by this session.

## -parameters

### -param pCryptoType [out]

Receives a GUID that specifies the encryption type. The following GUIDs are defined.

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

## -remarks

The application specifies the encryption type when it creates the session.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a>