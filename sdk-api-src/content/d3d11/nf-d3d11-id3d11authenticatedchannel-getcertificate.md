---
UID: NF:d3d11.ID3D11AuthenticatedChannel.GetCertificate
title: ID3D11AuthenticatedChannel::GetCertificate (d3d11.h)
author: windows-sdk-content
description: Gets the driver's certificate chain.
old-location: mf\id3d11authenticatedchannel_getcertificate.htm
tech.root: medfound
ms.assetid: D7FC07CA-B045-4C44-B3FD-B902C5437E47
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCertificate, GetCertificate method [Media Foundation], GetCertificate method [Media Foundation],ID3D11AuthenticatedChannel interface, ID3D11AuthenticatedChannel interface [Media Foundation],GetCertificate method, ID3D11AuthenticatedChannel.GetCertificate, ID3D11AuthenticatedChannel::GetCertificate, d3d11/ID3D11AuthenticatedChannel::GetCertificate, mf.id3d11authenticatedchannel_getcertificate
ms.topic: method
f1_keywords: ["d3d11/ID3D11AuthenticatedChannel.GetCertificate"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11AuthenticatedChannel.GetCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11AuthenticatedChannel::GetCertificate


## -description


Gets the driver's certificate chain.


## -parameters




### -param CertificateSize [in]

The size of the <i>pCertificate</i> array, in bytes. To get the size of the certificate chain, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize">ID3D11CryptoSession::GetCertificateSize</a>.


### -param pCertificate [out]

A pointer to a byte array that receives the driver's certificate chain. The caller must allocate the array.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/getcertificatesize">GetCertificateSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel">ID3D11AuthenticatedChannel</a>
 

 

