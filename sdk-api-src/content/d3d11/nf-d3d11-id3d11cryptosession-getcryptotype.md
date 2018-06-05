---
UID: NF:d3d11.ID3D11CryptoSession.GetCryptoType
title: ID3D11CryptoSession::GetCryptoType
author: windows-sdk-content
description: Gets the type of encryption that is supported by this session.
old-location: mf\id3d11cryptosession_getcryptotype.htm
old-project: medfound
ms.assetid: D5F62BFA-EA46-4BDD-8D8C-5D9D5BB590B9
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: D3D11_CRYPTO_TYPE_AES128_CTR, GetCryptoType, GetCryptoType method [Media Foundation], GetCryptoType method [Media Foundation],ID3D11CryptoSession interface, ID3D11CryptoSession interface [Media Foundation],GetCryptoType method, ID3D11CryptoSession.GetCryptoType, ID3D11CryptoSession::GetCryptoType, d3d11/ID3D11CryptoSession::GetCryptoType, mf.id3d11cryptosession_getcryptotype
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.h
api_name:
-	ID3D11CryptoSession.GetCryptoType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 


## -returns



This method does not return a value.




## -remarks



The application specifies the encryption type when it creates the session.




## -see-also




<a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a>
 

 

