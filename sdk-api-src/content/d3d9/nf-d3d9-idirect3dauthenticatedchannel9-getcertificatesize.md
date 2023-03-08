---
UID: NF:d3d9.IDirect3DAuthenticatedChannel9.GetCertificateSize
title: IDirect3DAuthenticatedChannel9::GetCertificateSize (d3d9.h)
description: Gets the size of the driver's certificate chain. (IDirect3DAuthenticatedChannel9.GetCertificateSize)
helpviewer_keywords: ["GetCertificateSize","GetCertificateSize method [Media Foundation]","GetCertificateSize method [Media Foundation]","IDirect3DAuthenticatedChannel9 interface","IDirect3DAuthenticatedChannel9 interface [Media Foundation]","GetCertificateSize method","IDirect3DAuthenticatedChannel9.GetCertificateSize","IDirect3DAuthenticatedChannel9::GetCertificateSize","d3d9/IDirect3DAuthenticatedChannel9::GetCertificateSize","mf.idirect3dauthenticatedchannel9_getcertificatesize"]
old-location: mf\idirect3dauthenticatedchannel9_getcertificatesize.htm
tech.root: mf
ms.assetid: a320a7be-6a0f-4de1-afc2-11eb2d7c24d6
ms.date: 12/05/2018
ms.keywords: GetCertificateSize, GetCertificateSize method [Media Foundation], GetCertificateSize method [Media Foundation],IDirect3DAuthenticatedChannel9 interface, IDirect3DAuthenticatedChannel9 interface [Media Foundation],GetCertificateSize method, IDirect3DAuthenticatedChannel9.GetCertificateSize, IDirect3DAuthenticatedChannel9::GetCertificateSize, d3d9/IDirect3DAuthenticatedChannel9::GetCertificateSize, mf.idirect3dauthenticatedchannel9_getcertificatesize
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
 - IDirect3DAuthenticatedChannel9::GetCertificateSize
 - d3d9/IDirect3DAuthenticatedChannel9::GetCertificateSize
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
 - IDirect3DAuthenticatedChannel9.GetCertificateSize
---

# IDirect3DAuthenticatedChannel9::GetCertificateSize


## -description

Gets the size of the driver's certificate chain.

## -parameters

### -param pCertificateSize

Receives the size of the certificate chain, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To get the certificate chain, call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate">IDirect3DAuthenticatedChannel9::GetCertificate</a>.

This method fails if the channel type is <b>D3DAUTHENTICATEDCHANNEL_D3D9</b>, because the Direct3D 9 channel does not support authentication.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9">IDirect3DAuthenticatedChannel9</a>
