---
UID: NN:dxvahd.IDXVAHD_Device
title: IDXVAHD_Device
author: windows-sdk-content
description: Represents a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\idxvahd_device.htm
old-project: medfound
ms.assetid: 3f79ac9c-2aed-4e1c-bf6f-02f9c54d59cd
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IDXVAHD_Device, IDXVAHD_Device interface [Media Foundation], IDXVAHD_Device interface [Media Foundation],described, dxvahd/IDXVAHD_Device, mf.idxvahd_device
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxvahd.h
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
tech.root: 
req.typenames: DXVAHD_SURFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxvahd.h
api_name:
-	IDXVAHD_Device
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXVAHD_Device interface


## -description


Represents a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

To get a pointer to this interface, call the <a href="https://msdn.microsoft.com/9a5411f9-2018-4a8a-922d-ab431d615583">DXVAHD_CreateDevice</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXVAHD_Device</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDXVAHD_Device</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXVAHD_Device</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/903e2c05-e4d4-42ca-a28d-6d4738ae6cfc">CreateVideoProcessor</a>
</td>
<td align="left" width="63%">
Creates a DXVA-HD video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c467a077-104c-443d-896b-d69441aa5160">CreateVideoSurface</a>
</td>
<td align="left" width="63%">
Creates one or more Microsoft Direct3D video surfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451674">GetVideoProcessorCaps</a>
</td>
<td align="left" width="63%">
Gets the capabilities of one or more DXVA-HD video processors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63e835bb-dda2-4449-8474-219a373da82d">GetVideoProcessorCustomRates</a>
</td>
<td align="left" width="63%">
Gets a list of custom rates that a DXVA-HD video process supports. Custom rates are used for frame-rate conversion and inverse telecine (IVTC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">GetVideoProcessorDeviceCaps</a>
</td>
<td align="left" width="63%">
Gets the capabilities of the DXVA-HD device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451689">GetVideoProcessorFilterRange</a>
</td>
<td align="left" width="63%">
Gets the range of values for an image filter that the DXVA-HD device supports.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b660d111-7bd1-4345-b229-1825d830bab4">GetVideoProcessorInputFormats</a>
</td>
<td align="left" width="63%">
Gets a list of the input formats supported by the DXVA-HD device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e701014d-c112-42fa-9bf5-88cb31424006">GetVideoProcessorOutputFormats</a>
</td>
<td align="left" width="63%">
Gets a list of the input formats supported by the DXVA-HD device.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/adddf378-f71c-4f81-bcf1-5d729a03eb58">Direct3D Video Interfaces</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

