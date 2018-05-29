---
UID: NF:d3d9.IDirect3DAuthenticatedChannel9.NegotiateKeyExchange
title: IDirect3DAuthenticatedChannel9::NegotiateKeyExchange
author: windows-sdk-content
description: Establishes a session key for the authenticated channel.
old-location: mf\idirect3dauthenticatedchannel9_negotiatekeyexchange.htm
old-project: medfound
ms.assetid: 35605d35-76c9-43d7-a022-6db6af179c41
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IDirect3DAuthenticatedChannel9 interface [Media Foundation],NegotiateKeyExchange method, IDirect3DAuthenticatedChannel9.NegotiateKeyExchange, IDirect3DAuthenticatedChannel9::NegotiateKeyExchange, NegotiateKeyExchange, NegotiateKeyExchange method [Media Foundation], NegotiateKeyExchange method [Media Foundation],IDirect3DAuthenticatedChannel9 interface, d3d9/IDirect3DAuthenticatedChannel9::NegotiateKeyExchange, mf.idirect3dauthenticatedchannel9_negotiatekeyexchange
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d9.h
api_name:
-	IDirect3DAuthenticatedChannel9.NegotiateKeyExchange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirect3DAuthenticatedChannel9::NegotiateKeyExchange


## -description


Establishes a session key for the authenticated channel.


## -parameters




### -param DataSize

The size of the data in the <i>pData</i> array, in bytes.


### -param pData

A pointer to a byte array that contains the encrypted session key. The buffer must contain 256 bytes of data, encrypted using RSA Encryption Scheme - Optimal Asymmetric Encryption Padding (RSAES-OAEP).


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method fails if the channel type is <b>D3DAUTHENTICATEDCHANNEL_D3D9</b>, because the Direct3D 9 channel does not support authentication.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/dd969956-a140-44ed-9917-5a0a09a432fa">IDirect3DAuthenticatedChannel9</a>
 

 

