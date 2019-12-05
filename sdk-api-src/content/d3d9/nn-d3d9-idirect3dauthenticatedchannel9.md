---
UID: NN:d3d9.IDirect3DAuthenticatedChannel9
title: IDirect3DAuthenticatedChannel9 (d3d9.h)
description: Provides a communication channel with the graphics driver or the Direct3D runtime.To get a pointer to this interface, call IDirect3DDevice9Video::CreateAuthenticatedChannel.
old-location: mf\idirect3dauthenticatedchannel9.htm
tech.root: medfound
ms.assetid: dd969956-a140-44ed-9917-5a0a09a432fa
ms.date: 12/05/2018
ms.keywords: IDirect3DAuthenticatedChannel9, IDirect3DAuthenticatedChannel9 interface [Media Foundation], IDirect3DAuthenticatedChannel9 interface [Media Foundation],described, d3d9/IDirect3DAuthenticatedChannel9, mf.idirect3dauthenticatedchannel9
ms.topic: interface
f1_keywords:
- d3d9/IDirect3DAuthenticatedChannel9
dev_langs:
- c++
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- d3d9.h
api_name:
- IDirect3DAuthenticatedChannel9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DAuthenticatedChannel9 interface


## -description


Provides a communication channel with the graphics driver or the Direct3D runtime.

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel">IDirect3DDevice9Video::CreateAuthenticatedChannel</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DAuthenticatedChannel9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DAuthenticatedChannel9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DAuthenticatedChannel9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate"> GetCertificate</a>
</td>
<td align="left" width="63%">
Gets the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange"> NegotiateKeyExchange</a>
</td>
<td align="left" width="63%">
Establishes a session key for the authenticated channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure">Configure</a>
</td>
<td align="left" width="63%">
Sends a configuration command to the authenticated channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize">GetCertificateSize</a>
</td>
<td align="left" width="63%">
Gets the size of the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query">Query</a>
</td>
<td align="left" width="63%">
Sends a query to the authenticated channel.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-video-interfaces">Direct3D Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>
 

 

