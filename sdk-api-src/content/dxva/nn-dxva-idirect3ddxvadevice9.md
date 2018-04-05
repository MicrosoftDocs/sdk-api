---
UID: NN:dxva.IDirect3DDXVADevice9
title: IDirect3DDXVADevice9
author: windows-driver-content
description: Represents a hardware accelerator for DirectX Video Acceleration (DXVA) 1.0.
old-location: mf\idirect3ddxvadevice9.htm
old-project: medfound
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IDirect3DDXVADevice9, IDirect3DDXVADevice9 interface [Media Foundation], IDirect3DDXVADevice9 interface [Media Foundation], described, dxva/IDirect3DDXVADevice9, mf.idirect3ddxvadevice9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COPP_TVProtectionStandard
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva.h
api_name:
-	IDirect3DDXVADevice9
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DDXVADevice9 interface


## -description


Represents a hardware accelerator for DirectX Video Acceleration (DXVA) 1.0.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DDXVADevice9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DDXVADevice9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DDXVADevice9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80471cc6-c66d-49d9-8593-780e41ac39b9">BeginFrame</a>
</td>
<td align="left" width="63%">
Begins the processing to create a decoded picture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b47cd53-6ce0-47b0-83ed-84926e92430f">EndFrame</a>
</td>
<td align="left" width="63%">
Ends the processing to create a decoded picture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543208">Execute</a>
</td>
<td align="left" width="63%">
Performs a DXVA decoding operation.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a4c3173-5911-49ec-8cb8-e30f96a4f1c9">QueryStatus</a>
</td>
<td align="left" width="63%">
Queries the read/write status of a DXVA decoding surface.
      

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/aeebf65f-1bde-4a33-87cd-25c62dcc0248">IDirect3DVideoDevice9::CreateDXVADevice</a>.




## -see-also




<a href="https://msdn.microsoft.com/adddf378-f71c-4f81-bcf1-5d729a03eb58">Direct3D Video Interfaces</a>
 

 

