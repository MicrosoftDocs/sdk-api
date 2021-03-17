---
UID: NF:d3d11.ID3D11CryptoSession.GetCryptoSessionHandle
title: ID3D11CryptoSession::GetCryptoSessionHandle (d3d11.h)
description: Gets a handle to the cryptographic session.
helpviewer_keywords: ["GetCryptoSessionHandle","GetCryptoSessionHandle method [Media Foundation]","GetCryptoSessionHandle method [Media Foundation]","ID3D11CryptoSession interface","ID3D11CryptoSession interface [Media Foundation]","GetCryptoSessionHandle method","ID3D11CryptoSession.GetCryptoSessionHandle","ID3D11CryptoSession::GetCryptoSessionHandle","d3d11/ID3D11CryptoSession::GetCryptoSessionHandle","mf.id3d11cryptosession_getcryptosessionhandle"]
old-location: mf\id3d11cryptosession_getcryptosessionhandle.htm
tech.root: mf
ms.assetid: AEF55A0B-7052-4264-BC82-DACE06D20A81
ms.date: 12/05/2018
ms.keywords: GetCryptoSessionHandle, GetCryptoSessionHandle method [Media Foundation], GetCryptoSessionHandle method [Media Foundation],ID3D11CryptoSession interface, ID3D11CryptoSession interface [Media Foundation],GetCryptoSessionHandle method, ID3D11CryptoSession.GetCryptoSessionHandle, ID3D11CryptoSession::GetCryptoSessionHandle, d3d11/ID3D11CryptoSession::GetCryptoSessionHandle, mf.id3d11cryptosession_getcryptosessionhandle
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
 - ID3D11CryptoSession::GetCryptoSessionHandle
 - d3d11/ID3D11CryptoSession::GetCryptoSessionHandle
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
 - ID3D11CryptoSession.GetCryptoSessionHandle
---

# ID3D11CryptoSession::GetCryptoSessionHandle


## -description

Gets a handle to the cryptographic session.

## -parameters

### -param pCryptoSessionHandle [out]

Receives a handle to the session.

## -remarks

You can use this handle to associate the session with a decoder. This enables the decoder to decrypt data that is encrypted using this session.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a>