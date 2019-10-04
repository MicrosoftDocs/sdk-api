---
UID: NN:d3d11.ID3D11CryptoSession
title: ID3D11CryptoSession (d3d11.h)
author: windows-sdk-content
description: Represents a cryptographic session.
old-location: mf\id3d11cryptosession.htm
tech.root: medfound
ms.assetid: E17F39CB-61E3-44EF-805D-AD386743744E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11CryptoSession, ID3D11CryptoSession interface [Media Foundation], ID3D11CryptoSession interface [Media Foundation],described, d3d11/ID3D11CryptoSession, mf.id3d11cryptosession
ms.topic: interface
f1_keywords: 
 - "d3d11/ID3D11CryptoSession"
dev_langs:
 - c++
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
 - ID3D11CryptoSession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11CryptoSession interface


## -description


Represents a cryptographic session.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11CryptoSession</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11CryptoSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11CryptoSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate">GetCertificate</a>
</td>
<td align="left" width="63%">
Gets the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize">GetCertificateSize</a>
</td>
<td align="left" width="63%">
Gets the size of the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle">GetCryptoSessionHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the cryptographic session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptotype">GetCryptoType</a>
</td>
<td align="left" width="63%">
Gets the type of encryption that is supported by this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getdecoderprofile">GetDecoderProfile</a>
</td>
<td align="left" width="63%">
Gets the decoding profile of the session.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession">ID3D11VideoDevice::CreateCryptoSession</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
 

 

