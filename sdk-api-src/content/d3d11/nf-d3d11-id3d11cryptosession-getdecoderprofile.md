---
UID: NF:d3d11.ID3D11CryptoSession.GetDecoderProfile
title: ID3D11CryptoSession::GetDecoderProfile (d3d11.h)
description: Gets the decoding profile of the session.
helpviewer_keywords: ["GetDecoderProfile","GetDecoderProfile method [Media Foundation]","GetDecoderProfile method [Media Foundation]","ID3D11CryptoSession interface","ID3D11CryptoSession interface [Media Foundation]","GetDecoderProfile method","ID3D11CryptoSession.GetDecoderProfile","ID3D11CryptoSession::GetDecoderProfile","d3d11/ID3D11CryptoSession::GetDecoderProfile","mf.id3d11cryptosession_getdecoderprofile"]
old-location: mf\id3d11cryptosession_getdecoderprofile.htm
tech.root: mf
ms.assetid: 358025E4-FC6E-4ED1-B02A-ED875DE76BCF
ms.date: 12/05/2018
ms.keywords: GetDecoderProfile, GetDecoderProfile method [Media Foundation], GetDecoderProfile method [Media Foundation],ID3D11CryptoSession interface, ID3D11CryptoSession interface [Media Foundation],GetDecoderProfile method, ID3D11CryptoSession.GetDecoderProfile, ID3D11CryptoSession::GetDecoderProfile, d3d11/ID3D11CryptoSession::GetDecoderProfile, mf.id3d11cryptosession_getdecoderprofile
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
 - ID3D11CryptoSession::GetDecoderProfile
 - d3d11/ID3D11CryptoSession::GetDecoderProfile
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
 - ID3D11CryptoSession.GetDecoderProfile
---

# ID3D11CryptoSession::GetDecoderProfile


## -description

Gets the decoding profile of the session.

## -parameters

### -param pDecoderProfile [out]

Receives the decoding profile. For a list of possible values, see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile">ID3D11VideoDevice::GetVideoDecoderProfile</a>.

## -remarks

The application specifies the profile when it creates the session.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a>