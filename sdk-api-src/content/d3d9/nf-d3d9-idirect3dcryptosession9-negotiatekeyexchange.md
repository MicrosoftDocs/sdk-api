---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirect3DCryptoSession9::NegotiateKeyExchange


## -description


Establishes the session key for the cryptographic session.


## -parameters




### -param DataSize

The size of the <i>pData</i> byte array, in bytes.


### -param pData

A pointer to a byte array that contains the encrypted session key.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To find out which key-exchange mechanism to use, call  the <a href="https://msdn.microsoft.com/4093e64c-340d-4f66-97ed-45bae3b259eb">IDirect3DDevice9Video::GetContentProtectionCaps</a>  method. The key-exchange mechanism is specified in the <b>KeyExchangeType</b>  member of the <a href="https://msdn.microsoft.com/73ef2e12-d376-4bc2-a940-d421acfdd43e">D3DCONTENTPROTECTIONCAPS</a> structure. If the value is <b>D3DKEYEXCHANGE_RSAES_OAEP</b>, use RSA Encryption Scheme - Optimal Asymmetric Encryption Padding (RSAES-OAEP) to encrypt the session key. Pass this encrypted cyphertext in the <i>pData</i> parameter.

If the key-exchange type is <b>D3DKEYEXCHANGE_DXVA</b>, do not call this method to establish the session key. Instead, use the key-exchange mechanism that is defined for DirectX Video Acceleration 2 (DXVA-2) decoding.

The driver might also use a proprietary key-exhange mechanism.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/2511c9da-e696-4e49-b180-7fc1317c1652">IDirect3DCryptoSession9</a>
 

 

