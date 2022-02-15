---
UID: NF:d3d11.ID3D11VideoContext.NegotiateCryptoSessionKeyExchange
title: ID3D11VideoContext::NegotiateCryptoSessionKeyExchange (d3d11.h)
description: Establishes the session key for a cryptographic session.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","NegotiateCryptoSessionKeyExchange method","ID3D11VideoContext.NegotiateCryptoSessionKeyExchange","ID3D11VideoContext::NegotiateCryptoSessionKeyExchange","NegotiateCryptoSessionKeyExchange","NegotiateCryptoSessionKeyExchange method [Media Foundation]","NegotiateCryptoSessionKeyExchange method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::NegotiateCryptoSessionKeyExchange","mf.id3d11videocontext_negotiatecryptosessionkeyexchange"]
old-location: mf\id3d11videocontext_negotiatecryptosessionkeyexchange.htm
tech.root: mf
ms.assetid: 76160B03-6F7F-4618-859B-0A7E73540CA4
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],NegotiateCryptoSessionKeyExchange method, ID3D11VideoContext.NegotiateCryptoSessionKeyExchange, ID3D11VideoContext::NegotiateCryptoSessionKeyExchange, NegotiateCryptoSessionKeyExchange, NegotiateCryptoSessionKeyExchange method [Media Foundation], NegotiateCryptoSessionKeyExchange method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::NegotiateCryptoSessionKeyExchange, mf.id3d11videocontext_negotiatecryptosessionkeyexchange
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
 - ID3D11VideoContext::NegotiateCryptoSessionKeyExchange
 - d3d11/ID3D11VideoContext::NegotiateCryptoSessionKeyExchange
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
 - ID3D11VideoContext.NegotiateCryptoSessionKeyExchange
---

# ID3D11VideoContext::NegotiateCryptoSessionKeyExchange


## -description

Establishes the session key for a cryptographic session.

## -parameters

### -param pCryptoSession [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> interface of the cryptographic session.

### -param DataSize [in]

The size of the <i>pData</i> byte array, in bytes.

### -param pData [in, out]

A pointer to a byte array that contains the encrypted session key.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The key exchange mechanism depends on the type of cryptographic session.

For RSA Encryption Scheme - Optimal Asymmetric Encryption Padding (RSAES-OAEP), the software decoder generates the secret key, encrypts the secret key by using the public key with RSAES-OAEP, and places the cipher text in the <i>pData</i> parameter. The actual size of the buffer for RSAES-OAEP is 256 bytes.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>