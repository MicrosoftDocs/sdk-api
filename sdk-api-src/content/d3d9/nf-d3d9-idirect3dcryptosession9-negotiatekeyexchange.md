---
UID: NF:d3d9.IDirect3DCryptoSession9.NegotiateKeyExchange
title: IDirect3DCryptoSession9::NegotiateKeyExchange (d3d9.h)
description: Establishes the session key for the cryptographic session.
helpviewer_keywords: ["IDirect3DCryptoSession9 interface [Media Foundation]","NegotiateKeyExchange method","IDirect3DCryptoSession9.NegotiateKeyExchange","IDirect3DCryptoSession9::NegotiateKeyExchange","NegotiateKeyExchange","NegotiateKeyExchange method [Media Foundation]","NegotiateKeyExchange method [Media Foundation]","IDirect3DCryptoSession9 interface","d3d9/IDirect3DCryptoSession9::NegotiateKeyExchange","mf.idirect3dcryptosession9_negotiatekeyexchange"]
old-location: mf\idirect3dcryptosession9_negotiatekeyexchange.htm
tech.root: mf
ms.assetid: 9e12f169-b121-400d-9244-8d7d0097c030
ms.date: 12/05/2018
ms.keywords: IDirect3DCryptoSession9 interface [Media Foundation],NegotiateKeyExchange method, IDirect3DCryptoSession9.NegotiateKeyExchange, IDirect3DCryptoSession9::NegotiateKeyExchange, NegotiateKeyExchange, NegotiateKeyExchange method [Media Foundation], NegotiateKeyExchange method [Media Foundation],IDirect3DCryptoSession9 interface, d3d9/IDirect3DCryptoSession9::NegotiateKeyExchange, mf.idirect3dcryptosession9_negotiatekeyexchange
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DCryptoSession9::NegotiateKeyExchange
 - d3d9/IDirect3DCryptoSession9::NegotiateKeyExchange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3DCryptoSession9.NegotiateKeyExchange
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To find out which key-exchange mechanism to use, call  the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps">IDirect3DDevice9Video::GetContentProtectionCaps</a>  method. The key-exchange mechanism is specified in the <b>KeyExchangeType</b>  member of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps">D3DCONTENTPROTECTIONCAPS</a> structure. If the value is <b>D3DKEYEXCHANGE_RSAES_OAEP</b>, use RSA Encryption Scheme - Optimal Asymmetric Encryption Padding (RSAES-OAEP) to encrypt the session key. Pass this encrypted cyphertext in the <i>pData</i> parameter.

If the key-exchange type is <b>D3DKEYEXCHANGE_DXVA</b>, do not call this method to establish the session key. Instead, use the key-exchange mechanism that is defined for DirectX Video Acceleration 2 (DXVA-2) decoding.

The driver might also use a proprietary key-exchange mechanism.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a>