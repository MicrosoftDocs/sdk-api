---
UID: NN:d3d9.IDirect3DDevice9Video
title: IDirect3DDevice9Video (d3d9.h)
author: windows-sdk-content
description: Enables an application to use content protection and encryption services implemented by a graphics driver.To get a pointer to this interface, call QueryInterface on a D3D9Ex device.
old-location: mf\idirect3ddevice9video.htm
tech.root: medfound
ms.assetid: e2c9cd73-6320-4ce3-a44f-5658c162aeb4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirect3DDevice9Video, IDirect3DDevice9Video interface [Media Foundation], IDirect3DDevice9Video interface [Media Foundation],described, d3d9/IDirect3DDevice9Video, mf.idirect3ddevice9video
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
 - IDirect3DDevice9Video
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9Video interface


## -description


Enables an application to use content protection and encryption services implemented by a graphics driver.

To get a pointer to this interface, call <b>QueryInterface</b> on a D3D9Ex device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DDevice9Video</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DDevice9Video</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DDevice9Video</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0dcfc3f-ede3-4917-8806-6bd343154cf8">CreateAuthenticatedChannel</a>
</td>
<td align="left" width="63%">
Creates a channel to communicate with the Direct3D device or the graphics driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c0e3aa4-94d5-4398-a6c0-5466a437162d">CreateCryptoSession</a>
</td>
<td align="left" width="63%">
Creates a cryptographic session to encrypt video content that is sent to the display driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4093e64c-340d-4f66-97ed-45bae3b259eb">GetContentProtectionCaps</a>
</td>
<td align="left" width="63%">
Queries the display driver for its content protection capabilities.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/adddf378-f71c-4f81-bcf1-5d729a03eb58">Direct3D Video Interfaces</a>



<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>
 

 

