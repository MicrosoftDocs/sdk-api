---
UID: NN:dxva.IDirect3DVideoDevice9
title: IDirect3DVideoDevice9
author: windows-driver-content
description: Enables hardware-accelerated decoding from a Direct3D 9 device, using DirectX Video Acceleration (DXVA) version 1.0.
old-location: mf\idirect3dvideodevice9.htm
old-project: medfound
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IDirect3DVideoDevice9, IDirect3DVideoDevice9 interface [Media Foundation], IDirect3DVideoDevice9 interface [Media Foundation], described, dxva/IDirect3DVideoDevice9, mf.idirect3dvideodevice9
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
-	IDirect3DVideoDevice9
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DVideoDevice9 interface


## -description


Enables hardware-accelerated decoding from a Direct3D 9 device, using DirectX Video Acceleration (DXVA) version 1.0.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DVideoDevice9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DVideoDevice9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DVideoDevice9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aeebf65f-1bde-4a33-87cd-25c62dcc0248">CreateDXVADevice</a>
</td>
<td align="left" width="63%">
Creates a DXVA decoder device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh998978">CreateSurface</a>
</td>
<td align="left" width="63%">
Creates a compressed surface for DXVA decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a9fb077-fd79-4faa-a0f8-b3ac987adf36">GetDXVACompressedBufferInfo</a>
</td>
<td align="left" width="63%">
Gets information about the compressed buffers needed for hardware-accelerated decoding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4adbbac2-a25d-4e17-b62e-a02a67dcdbed">GetDXVAGuids</a>
</td>
<td align="left" width="63%">
Gets a list of the DXVA profiles that are supported by the display driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20e3dbef-daf5-487a-8d50-e2ebdb712cc0">GetDXVAInternalInfo</a>
</td>
<td align="left" width="63%">
Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c69ea5f-6054-4430-95b5-820db6854fc0">GetUncompressedDXVAFormats</a>
</td>
<td align="left" width="63%">
Gets a list of uncompressed pixel formats that can be rendered using a specified DXVA profile.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a> or <a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a> pointer.

This interface supports DXVA 1.0 only. It does not support DXVA 2.0.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=93647">DXVA 1.0 specification</a>



<a href="https://msdn.microsoft.com/adddf378-f71c-4f81-bcf1-5d729a03eb58">Direct3D Video Interfaces</a>



<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>
 

 

