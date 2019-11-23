---
UID: NE:d3d11_1.D3D11_CRYPTO_SESSION_STATUS
title: D3D11_CRYPTO_SESSION_STATUS (d3d11_1.h)

description: Represents the status of an ID3D11CryptoSession interface.
old-location: mf\d3d11_crypto_session_status.htm
tech.root: medfound
ms.assetid: C98DEC40-21D0-483A-A982-E6E19BBDE241

ms.date: 12/05/2018
ms.keywords: D3D11_CRYPTO_SESSION_STATUS, D3D11_CRYPTO_SESSION_STATUS enumeration [Media Foundation], D3D11_CRYPTO_SESSION_STATUS_KEY_AND_CONTENT_LOST, D3D11_CRYPTO_SESSION_STATUS_KEY_LOST, D3D11_CRYPTO_SESSION_STATUS_OK, d3d11_1/D3D11_CRYPTO_SESSION_STATUS, d3d11_1/D3D11_CRYPTO_SESSION_STATUS_KEY_AND_CONTENT_LOST, d3d11_1/D3D11_CRYPTO_SESSION_STATUS_KEY_LOST, d3d11_1/D3D11_CRYPTO_SESSION_STATUS_OK, mf.d3d11_crypto_session_status
ms.topic: enum
f1_keywords: 
 - "d3d11_1/D3D11_CRYPTO_SESSION_STATUS"
dev_langs:
 - c++
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_1.h
api_name:
 - D3D11_CRYPTO_SESSION_STATUS
targetos: Windows
req.typenames: D3D11_CRYPTO_SESSION_STATUS
req.redist: 
ms.custom: 19H1
---

# D3D11_CRYPTO_SESSION_STATUS enumeration


## -description


Represents the status of an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> interface.


## -enum-fields




### -field D3D11_CRYPTO_SESSION_STATUS_OK

The <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> is in a functional state.


### -field D3D11_CRYPTO_SESSION_STATUS_KEY_LOST

The underlying hardware key for the specified <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> has become lost.


### -field D3D11_CRYPTO_SESSION_STATUS_KEY_AND_CONTENT_LOST

The underlying hardware key for the specified <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession">ID3D11CryptoSession</a> has become lost and protected content has become corrupted. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
 

 

