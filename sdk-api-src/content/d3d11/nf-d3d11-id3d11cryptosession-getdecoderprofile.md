---
UID: NF:d3d11.ID3D11CryptoSession.GetDecoderProfile
title: ID3D11CryptoSession::GetDecoderProfile
author: windows-sdk-content
description: Gets the decoding profile of the session.
old-location: mf\id3d11cryptosession_getdecoderprofile.htm
old-project: medfound
ms.assetid: 358025E4-FC6E-4ED1-B02A-ED875DE76BCF
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetDecoderProfile, GetDecoderProfile method [Media Foundation], GetDecoderProfile method [Media Foundation],ID3D11CryptoSession interface, ID3D11CryptoSession interface [Media Foundation],GetDecoderProfile method, ID3D11CryptoSession.GetDecoderProfile, ID3D11CryptoSession::GetDecoderProfile, d3d11/ID3D11CryptoSession::GetDecoderProfile, mf.id3d11cryptosession_getdecoderprofile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11CryptoSession.GetDecoderProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11CryptoSession::GetDecoderProfile


## -description


Gets the decoding profile of the session.


## -parameters




### -param pDecoderProfile [out]

Receives the decoding profile. For a list of possible values, see <a href="https://msdn.microsoft.com/8D958469-7FC3-4B4F-82BF-271662CF0088">ID3D11VideoDevice::GetVideoDecoderProfile</a>. 


## -returns



This method does not return a value.




## -remarks



The application specifies the profile when it creates the session.




## -see-also




<a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a>
 

 

