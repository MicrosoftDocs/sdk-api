---
UID: NF:d3d9.IDirect3DAuthenticatedChannel9.GetCertificate
title: IDirect3DAuthenticatedChannel9::GetCertificate (d3d9.h)
description: Gets the driver's certificate chain. (IDirect3DAuthenticatedChannel9.GetCertificate)
helpviewer_keywords: ["GetCertificate","GetCertificate method [Media Foundation]","GetCertificate method [Media Foundation]","IDirect3DAuthenticatedChannel9 interface","IDirect3DAuthenticatedChannel9 interface [Media Foundation]","GetCertificate method","IDirect3DAuthenticatedChannel9.GetCertificate","IDirect3DAuthenticatedChannel9::GetCertificate","d3d9/IDirect3DAuthenticatedChannel9::GetCertificate","mf.idirect3dauthenticatedchannel9_getcertificate"]
old-location: mf\idirect3dauthenticatedchannel9_getcertificate.htm
tech.root: mf
ms.assetid: 0663d3a0-256b-4c96-aca7-06c4d1853554
ms.date: 12/05/2018
ms.keywords: GetCertificate, GetCertificate method [Media Foundation], GetCertificate method [Media Foundation],IDirect3DAuthenticatedChannel9 interface, IDirect3DAuthenticatedChannel9 interface [Media Foundation],GetCertificate method, IDirect3DAuthenticatedChannel9.GetCertificate, IDirect3DAuthenticatedChannel9::GetCertificate, d3d9/IDirect3DAuthenticatedChannel9::GetCertificate, mf.idirect3dauthenticatedchannel9_getcertificate
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
 - IDirect3DAuthenticatedChannel9::GetCertificate
 - d3d9/IDirect3DAuthenticatedChannel9::GetCertificate
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
 - IDirect3DAuthenticatedChannel9.GetCertificate
---

# IDirect3DAuthenticatedChannel9::GetCertificate


## -description

Gets the driver's certificate chain.

## -parameters

### -param CertifacteSize

The size of the <i>ppCertificate</i> array, in bytes. To get the size of the certificate chain, call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize">IDirect3DAuthenticatedChannel9::GetCertificateSize</a>.

### -param ppCertificate

A pointer to a byte array that receives the driver's X.509 certificate chain. The caller must allocate the array.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use the certificate chain to verify that the driver's certificate was signed by Microsoft and has not been revoked. The driver's certificate also contains the driver's public key. Use the public key to establish a session key, by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange">IDirect3DAuthenticatedChannel9::NegotiateKeyExchange</a> method.

This method fails if the channel type is <b>D3DAUTHENTICATEDCHANNEL_D3D9</b>, because the Direct3D 9 channel does not support authentication.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9">IDirect3DAuthenticatedChannel9</a>
