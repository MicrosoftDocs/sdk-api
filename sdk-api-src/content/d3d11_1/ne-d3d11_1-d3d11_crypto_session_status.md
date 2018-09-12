---
UID: NE:d3d11_1.D3D11_CRYPTO_SESSION_STATUS
title: D3D11_CRYPTO_SESSION_STATUS
author: windows-sdk-content
description: Represents the status of an ID3D11CryptoSession interface.
old-location: mf\d3d11_crypto_session_status.htm
tech.root: medfound
ms.assetid: C98DEC40-21D0-483A-A982-E6E19BBDE241
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: D3D11_CRYPTO_SESSION_STATUS, D3D11_CRYPTO_SESSION_STATUS enumeration [Media Foundation], D3D11_CRYPTO_SESSION_STATUS_KEY_AND_CONTENT_LOST, D3D11_CRYPTO_SESSION_STATUS_KEY_LOST, D3D11_CRYPTO_SESSION_STATUS_OK, d3d11_1/D3D11_CRYPTO_SESSION_STATUS, d3d11_1/D3D11_CRYPTO_SESSION_STATUS_KEY_AND_CONTENT_LOST, d3d11_1/D3D11_CRYPTO_SESSION_STATUS_KEY_LOST, d3d11_1/D3D11_CRYPTO_SESSION_STATUS_OK, mf.d3d11_crypto_session_status
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: D3D11_CRYPTO_SESSION_STATUS
req.redist: 
---

# D3D11_CRYPTO_SESSION_STATUS enumeration


## -description


Represents the status of an <a href="https://msdn.microsoft.com/en-us/library/Hh447691(v=VS.85).aspx">ID3D11CryptoSession</a> interface.


## -enum-fields




### -field D3D11_CRYPTO_SESSION_STATUS_OK

The <a href="https://msdn.microsoft.com/en-us/library/Hh447691(v=VS.85).aspx">ID3D11CryptoSession</a> is in a functional state.


### -field D3D11_CRYPTO_SESSION_STATUS_KEY_LOST

The underlying hardware key for the specified <a href="https://msdn.microsoft.com/en-us/library/Hh447691(v=VS.85).aspx">ID3D11CryptoSession</a> has become lost.


### -field D3D11_CRYPTO_SESSION_STATUS_KEY_AND_CONTENT_LOST

The underlying hardware key for the specified <a href="https://msdn.microsoft.com/en-us/library/Hh447691(v=VS.85).aspx">ID3D11CryptoSession</a> has become lost and protected content has become corrupted. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447678(v=VS.85).aspx">Direct3D 11 Video Enumerations</a>
 

 

