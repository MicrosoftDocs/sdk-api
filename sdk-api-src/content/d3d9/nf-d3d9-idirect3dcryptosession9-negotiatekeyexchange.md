---
UID: NF:d3d9.IDirect3DCryptoSession9.NegotiateKeyExchange
title: IDirect3DCryptoSession9::NegotiateKeyExchange
author: windows-sdk-content
description: Establishes the session key for the cryptographic session.
old-location: mf\idirect3dcryptosession9_negotiatekeyexchange.htm
tech.root: medfound
ms.assetid: 9e12f169-b121-400d-9244-8d7d0097c030
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDirect3DCryptoSession9 interface [Media Foundation],NegotiateKeyExchange method, IDirect3DCryptoSession9.NegotiateKeyExchange, IDirect3DCryptoSession9::NegotiateKeyExchange, NegotiateKeyExchange, NegotiateKeyExchange method [Media Foundation], NegotiateKeyExchange method [Media Foundation],IDirect3DCryptoSession9 interface, d3d9/IDirect3DCryptoSession9::NegotiateKeyExchange, mf.idirect3dcryptosession9_negotiatekeyexchange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - d3d9.h
api_name:
 - IDirect3DCryptoSession9.NegotiateKeyExchange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

