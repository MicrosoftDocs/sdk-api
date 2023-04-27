---
UID: NF:d3d11.ID3D11CryptoSession.GetCertificate
title: ID3D11CryptoSession::GetCertificate (d3d11.h)
description: Gets the driver's certificate chain. (ID3D11CryptoSession.GetCertificate)
helpviewer_keywords: ["GetCertificate","GetCertificate method [Media Foundation]","GetCertificate method [Media Foundation]","ID3D11CryptoSession interface","ID3D11CryptoSession interface [Media Foundation]","GetCertificate method","ID3D11CryptoSession.GetCertificate","ID3D11CryptoSession::GetCertificate","d3d11/ID3D11CryptoSession::GetCertificate","mf.id3d11cryptosession_getcertificate"]
old-location: mf\id3d11cryptosession_getcertificate.htm
tech.root: mf
ms.assetid: D6407570-62C0-45D0-9BCB-41EA007D86A6
ms.date: 12/05/2018
ms.keywords: GetCertificate, GetCertificate method [Media Foundation], GetCertificate method [Media Foundation],ID3D11CryptoSession interface, ID3D11CryptoSession interface [Media Foundation],GetCertificate method, ID3D11CryptoSession.GetCertificate, ID3D11CryptoSession::GetCertificate, d3d11/ID3D11CryptoSession::GetCertificate, mf.id3d11cryptosession_getcertificate
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
 - ID3D11CryptoSession::GetCertificate
 - d3d11/ID3D11CryptoSession::GetCertificate
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
 - ID3D11CryptoSession.GetCertificate
---

# ID3D11CryptoSession::GetCertificate


## -description

Gets the driver's certificate chain.

## -parameters

### -param CertificateSize [in]

The size of the <i>pCertificate</i> array, in bytes. To get the size of the certificate chain, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize">ID3D11CryptoSession::GetCertificateSize</a>.

### -param pCertificate [out]

A pointer to a byte array that receives the driver's certificate chain. The caller must allocate the array.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a>
