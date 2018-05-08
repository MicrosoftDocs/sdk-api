---
UID: NF:d3d11.ID3D11VideoContext.NegotiateCryptoSessionKeyExchange
title: ID3D11VideoContext::NegotiateCryptoSessionKeyExchange
author: windows-driver-content
description: Establishes the session key for a cryptographic session.
old-location: mf\id3d11videocontext_negotiatecryptosessionkeyexchange.htm
old-project: medfound
ms.assetid: 76160B03-6F7F-4618-859B-0A7E73540CA4
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],NegotiateCryptoSessionKeyExchange method, ID3D11VideoContext.NegotiateCryptoSessionKeyExchange, ID3D11VideoContext::NegotiateCryptoSessionKeyExchange, NegotiateCryptoSessionKeyExchange, NegotiateCryptoSessionKeyExchange method [Media Foundation], NegotiateCryptoSessionKeyExchange method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::NegotiateCryptoSessionKeyExchange, mf.id3d11videocontext_negotiatecryptosessionkeyexchange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.h
api_name:
-	ID3D11VideoContext.NegotiateCryptoSessionKeyExchange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::NegotiateCryptoSessionKeyExchange


## -description


Establishes the session key for a cryptographic session.




## -parameters




### -param pCryptoSession [in]

A pointer to the <a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a> interface of the cryptographic session.


### -param DataSize [in]

The size of the <i>pData</i> byte array, in bytes.




### -param pData [in, out]

A pointer to a byte array that contains the encrypted session key.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The key exchange mechanism depends on the type of cryptographic session.

For RSA Encryption Scheme - Optimal Asymmetric Encryption Padding (RSAES-OAEP), the software decoder generates the secret key, encrypts the secret key by using the public key with RSAES-OAEP, and places the cipher text in the <i>pData</i> parameter. The actual size of the buffer for RSAES-OAEP is 256 bytes.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

