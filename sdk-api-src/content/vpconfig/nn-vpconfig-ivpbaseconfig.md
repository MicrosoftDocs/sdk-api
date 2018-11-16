---
UID: NN:vpconfig.IVPBaseConfig
title: IVPBaseConfig
author: windows-sdk-content
description: IVPBaseConfig is implemented on a filter that wraps a hardware device such as a decoder or capture device, if the device has a video port to the graphics adapter.
old-location: dshow\ivpbaseconfig.htm
tech.root: DirectShow
ms.assetid: d9a4f395-3d2f-429a-884d-90131927a929
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVPBaseConfig, IVPBaseConfig interface [DirectShow], IVPBaseConfig interface [DirectShow],described, IVPBaseConfigInterface, dshow.ivpbaseconfig, vpconfig/IVPBaseConfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vpconfig.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseConfig interface


## -description



<code>IVPBaseConfig</code> is implemented on a filter that wraps a hardware device such as a decoder or capture device, if the device has a video port to the graphics adapter. This interface allows the video port to communicate with the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter regarding configuration information. The <a href="https://msdn.microsoft.com/2c0eb294-7e57-4d8d-98b1-57c3834279a0">IVPConfig</a> interface derives from this interface.

Applications should never use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPBaseConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVPBaseConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVPBaseConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b428e77a-83c3-42ce-95e4-1cdde4da066d">GetConnectInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the connections supported by the VPE object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b86ff2c-c51f-4498-a000-5f1868c2c24b">GetMaxPixelRate</a>
</td>
<td align="left" width="63%">
Retrieves the maximum pixel rate the device will output for a given width and height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4d4b63f-b84c-4831-b16e-c0042b54a215">GetOverlaySurface</a>
</td>
<td align="left" width="63%">
Queries whether the caller should use the driver's overlay surface, and if so, returns a pointer to the surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0426a2a-a856-4e5d-8ff2-4afa3b18355e">GetVideoFormats</a>
</td>
<td align="left" width="63%">
Retrieves the video formats the driver supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/385ab5e4-b904-4268-a97e-1c3e7789b0a2">GetVPDataInfo</a>
</td>
<td align="left" width="63%">
Retrieves the current video port data information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9b4ea2b-ad71-4226-9aad-e68a9cb26274">InformVPInputFormats</a>
</td>
<td align="left" width="63%">
Informs the device what video formats the video port supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e52bb213-e6e7-4bae-9e1e-6b34f34cf1d1">SetConnectInfo</a>
</td>
<td align="left" width="63%">
Sets the video port connection parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e180f731-a540-4754-93ff-232ad4502c6f">SetDDSurfaceKernelHandles</a>
</td>
<td align="left" width="63%">
Specifies the kernel-mode handles of the DirectDraw surfaces to be used for the overlay suface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3a04341-6cca-4fb4-bf47-30659d039a0d">SetDirectDrawKernelHandle</a>
</td>
<td align="left" width="63%">
Sets the kernel-mode handle to the DirectDraw object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c33cea2-2c83-4978-9059-c15706f14f85">SetInvertPolarity</a>
</td>
<td align="left" width="63%">
Reverses the current polarity the driver uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4af0092e-5866-45ca-b0be-e97d9dd51b0f">SetSurfaceParameters</a>
</td>
<td align="left" width="63%">
Informs the device of the layout of the overlay surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98b4182f-c286-4f4a-86b8-40d093456628">SetVideoFormat</a>
</td>
<td align="left" width="63%">
Sets the video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9be16349-b214-4441-8093-dfb0caa84507">SetVideoPortID</a>
</td>
<td align="left" width="63%">
Specifies the ID of the hardware video port to use.

</td>
</tr>
</table> 


## -remarks



Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/6b40ba9e-8562-4d31-beaf-e4d4858bf145">IVPNotify</a>
 

 

