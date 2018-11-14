---
UID: NN:strmif.IAMCameraControl
title: IAMCameraControl
author: windows-sdk-content
description: The IAMCameraControl interface controls camera settings such as zoom, pan, aperture adjustment, or shutter speed. To obtain this interface, query the filter that controls the camera.
old-location: dshow\iamcameracontrol.htm
tech.root: DirectShow
ms.assetid: 22bc35f1-76d4-4881-91d1-72f05c24561d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMCameraControl, IAMCameraControl interface [DirectShow], IAMCameraControl interface [DirectShow],described, IAMCameraControlInterface, dshow.iamcameracontrol, strmif/IAMCameraControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMCameraControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMCameraControl interface


## -description



The <b>IAMCameraControl</b> interface controls camera settings such as zoom, pan, aperture adjustment, or shutter speed. To obtain this interface, query the filter that controls the camera.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMCameraControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMCameraControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMCameraControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a21f207-5fbb-44b2-82d2-89be29dbdf2c">Get</a>
</td>
<td align="left" width="63%">
Gets the current setting of a camera property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f09090ea-d916-47cd-8621-e8c2bb46aeca">GetRange</a>
</td>
<td align="left" width="63%">
Gets the range and default value of a specified camera property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d896fb5e-a43b-4cb8-a5d1-4ce6e60831be">Set</a>
</td>
<td align="left" width="63%">
Sets a specified property on the camera.

</td>
</tr>
</table> 


## -remarks



For Windows Driver Model (WDM) devices, the <a href="https://msdn.microsoft.com/97432b99-e89b-4d69-963d-a959f887e580">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://msdn.microsoft.com/8899a474-fa6f-4d5c-bd68-2433428bb5c5">PROPSETID_VIDCAP_CAMERACONTROL</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.




## -see-also




<a href="https://msdn.microsoft.com/f789db78-292e-4092-a5dc-1906845fb1dd">Configure the Video Quality</a>
 

 

