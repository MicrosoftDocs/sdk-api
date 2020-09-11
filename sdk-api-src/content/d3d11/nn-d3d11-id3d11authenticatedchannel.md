---
UID: NN:d3d11.ID3D11AuthenticatedChannel
title: ID3D11AuthenticatedChannel (d3d11.h)
description: Provides a communication channel with the graphics driver or the Microsoft Direct3D runtime.
helpviewer_keywords: ["ID3D11AuthenticatedChannel","ID3D11AuthenticatedChannel interface [Media Foundation]","ID3D11AuthenticatedChannel interface [Media Foundation]","described","d3d11/ID3D11AuthenticatedChannel","mf.id3d11authenticatedchannel"]
old-location: mf\id3d11authenticatedchannel.htm
tech.root: mf
ms.assetid: B2DE8E06-1571-4D50-9296-8EB4BB74D6BA
ms.date: 12/05/2018
ms.keywords: ID3D11AuthenticatedChannel, ID3D11AuthenticatedChannel interface [Media Foundation], ID3D11AuthenticatedChannel interface [Media Foundation],described, d3d11/ID3D11AuthenticatedChannel, mf.id3d11authenticatedchannel
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
 - ID3D11AuthenticatedChannel
 - d3d11/ID3D11AuthenticatedChannel
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
 - ID3D11AuthenticatedChannel
---

# ID3D11AuthenticatedChannel interface


## -description

Provides a communication channel with the graphics driver or the Microsoft Direct3D runtime.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11AuthenticatedChannel</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11AuthenticatedChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11AuthenticatedChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificate">GetCertificate</a>
</td>
<td align="left" width="63%">
Gets the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificatesize">GetCertificateSize</a>
</td>
<td align="left" width="63%">
Gets the size of the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getchannelhandle">GetChannelHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the authenticated channel.

</td>
</tr>
</table>

## -remarks

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel">ID3D11VideoDevice::CreateAuthenticatedChannel</a>.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>

