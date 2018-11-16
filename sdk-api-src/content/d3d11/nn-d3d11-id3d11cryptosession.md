---
UID: NN:d3d11.ID3D11CryptoSession
title: ID3D11CryptoSession
author: windows-sdk-content
description: Represents a cryptographic session.
old-location: mf\id3d11cryptosession.htm
tech.root: medfound
ms.assetid: E17F39CB-61E3-44EF-805D-AD386743744E
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D11CryptoSession, ID3D11CryptoSession interface [Media Foundation], ID3D11CryptoSession interface [Media Foundation],described, d3d11/ID3D11CryptoSession, mf.id3d11cryptosession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11CryptoSession interface


## -description


Represents a cryptographic session.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11CryptoSession</b> interface inherits from <a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>. <b>ID3D11CryptoSession</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/D6407570-62C0-45D0-9BCB-41EA007D86A6">GetCertificate</a>
</td>
<td align="left" width="63%">
Gets the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C5FE51B8-A681-4B8C-BFC0-9D0B625292F1">GetCertificateSize</a>
</td>
<td align="left" width="63%">
Gets the size of the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AEF55A0B-7052-4264-BC82-DACE06D20A81">GetCryptoSessionHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the cryptographic session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D5F62BFA-EA46-4BDD-8D8C-5D9D5BB590B9">GetCryptoType</a>
</td>
<td align="left" width="63%">
Gets the type of encryption that is supported by this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/358025E4-FC6E-4ED1-B02A-ED875DE76BCF">GetDecoderProfile</a>
</td>
<td align="left" width="63%">
Gets the decoding profile of the session.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/384EE3E1-2B62-477B-8A3F-FDCD06959B74">ID3D11VideoDevice::CreateCryptoSession</a>.




## -see-also




<a href="https://msdn.microsoft.com/2AE97FFE-0FA4-4CC0-8433-7BA46BCACE30">Direct3D 11 Video Interfaces</a>



<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>
 

 

