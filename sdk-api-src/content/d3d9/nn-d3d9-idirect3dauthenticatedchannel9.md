---
UID: NN:d3d9.IDirect3DAuthenticatedChannel9
title: IDirect3DAuthenticatedChannel9
author: windows-sdk-content
description: Provides a communication channel with the graphics driver or the Direct3D runtime.To get a pointer to this interface, call IDirect3DDevice9Video::CreateAuthenticatedChannel.
old-location: mf\idirect3dauthenticatedchannel9.htm
tech.root: medfound
ms.assetid: dd969956-a140-44ed-9917-5a0a09a432fa
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDirect3DAuthenticatedChannel9, IDirect3DAuthenticatedChannel9 interface [Media Foundation], IDirect3DAuthenticatedChannel9 interface [Media Foundation],described, d3d9/IDirect3DAuthenticatedChannel9, mf.idirect3dauthenticatedchannel9
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DAuthenticatedChannel9 interface


## -description


Provides a communication channel with the graphics driver or the Direct3D runtime.

To get a pointer to this interface, call <a href="https://msdn.microsoft.com/e0dcfc3f-ede3-4917-8806-6bd343154cf8">IDirect3DDevice9Video::CreateAuthenticatedChannel</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DAuthenticatedChannel9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DAuthenticatedChannel9</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0663d3a0-256b-4c96-aca7-06c4d1853554"> GetCertificate</a>
</td>
<td align="left" width="63%">
Gets the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35605d35-76c9-43d7-a022-6db6af179c41"> NegotiateKeyExchange</a>
</td>
<td align="left" width="63%">
Establishes a session key for the authenticated channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12d15872-4f35-4a6d-ae99-bc9fa69ffe06">Configure</a>
</td>
<td align="left" width="63%">
Sends a configuration command to the authenticated channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a320a7be-6a0f-4de1-afc2-11eb2d7c24d6">GetCertificateSize</a>
</td>
<td align="left" width="63%">
Gets the size of the driver's certificate chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/370ed31d-5b75-4767-b8d8-33cb2ff49fee">Query</a>
</td>
<td align="left" width="63%">
Sends a query to the authenticated channel.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/adddf378-f71c-4f81-bcf1-5d729a03eb58">Direct3D Video Interfaces</a>



<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>
 

 

