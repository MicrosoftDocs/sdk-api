---
UID: NF:d3d9.IDirect3DCryptoSession9.GetCertificate
title: IDirect3DCryptoSession9::GetCertificate (d3d9.h)
description: Gets the driver's certificate chain. (IDirect3DCryptoSession9.GetCertificate)
helpviewer_keywords: ["GetCertificate","GetCertificate method [Media Foundation]","GetCertificate method [Media Foundation]","IDirect3DCryptoSession9 interface","IDirect3DCryptoSession9 interface [Media Foundation]","GetCertificate method","IDirect3DCryptoSession9.GetCertificate","IDirect3DCryptoSession9::GetCertificate","d3d9/IDirect3DCryptoSession9::GetCertificate","mf.idirect3dcryptosession9_getcertificate"]
old-location: mf\idirect3dcryptosession9_getcertificate.htm
tech.root: mf
ms.assetid: 802285a6-1338-4131-bb5e-9d4daad62bdc
ms.date: 12/05/2018
ms.keywords: GetCertificate, GetCertificate method [Media Foundation], GetCertificate method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],GetCertificate method, IDirect3DCryptoSession9.GetCertificate, IDirect3DCryptoSession9::GetCertificate, d3d9/IDirect3DCryptoSession9::GetCertificate, mf.idirect3dcryptosession9_getcertificate
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
 - IDirect3DCryptoSession9::GetCertificate
 - d3d9/IDirect3DCryptoSession9::GetCertificate
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
 - IDirect3DCryptoSession9.GetCertificate
---

# IDirect3DCryptoSession9::GetCertificate


## -description

Gets the driver's certificate chain.

## -parameters

### -param CertifacteSize

The size of the <i>ppCertificate</i> array, in bytes. To get the size of the certificate chain, call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize">IDirect3DCryptoSession9::GetCertificateSize</a>.

### -param ppCertificate

A pointer to a byte array that receives the driver's certificate chain. The caller must allocate the array.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The standard key-exchange mechanism uses the driver's Output Protection Manager (OPM) certificate, which is an X.509 certificate. The type of key exchange is given in the capabilities information returned by the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps">IDirect3DDevice9Video::GetContentProtectionCaps</a>  method. The key-exchange mechanism is specified by the <b>KeyExchangeType</b>  member of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps">D3DCONTENTPROTECTIONCAPS</a> structure. If the value is <b>D3DKEYEXCHANGE_RSAES_OAEP</b>, an X.509 certificate is used.

For other types of key exchange, the driver might use some other type of certificate, or might not provide a certificate.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a>
