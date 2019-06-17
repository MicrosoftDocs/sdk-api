---
UID: NN:vpconfig.IVPBaseConfig
title: IVPBaseConfig (vpconfig.h)
author: windows-sdk-content
description: IVPBaseConfig is implemented on a filter that wraps a hardware device such as a decoder or capture device, if the device has a video port to the graphics adapter.
old-location: dshow\ivpbaseconfig.htm
tech.root: DirectShow
ms.assetid: d9a4f395-3d2f-429a-884d-90131927a929
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVPBaseConfig, IVPBaseConfig interface [DirectShow], IVPBaseConfig interface [DirectShow],described, IVPBaseConfigInterface, dshow.ivpbaseconfig, vpconfig/IVPBaseConfig
ms.topic: interface
f1_keywords: ["vpconfig/IVPBaseConfig"]
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
ms.custom: 19H1
---

# IVPBaseConfig interface


## -description



<code>IVPBaseConfig</code> is implemented on a filter that wraps a hardware device such as a decoder or capture device, if the device has a video port to the graphics adapter. This interface allows the video port to communicate with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter regarding configuration information. The <a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig">IVPConfig</a> interface derives from this interface.

Applications should never use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPBaseConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVPBaseConfig</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-getconnectinfo">GetConnectInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the connections supported by the VPE object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-getmaxpixelrate">GetMaxPixelRate</a>
</td>
<td align="left" width="63%">
Retrieves the maximum pixel rate the device will output for a given width and height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-getoverlaysurface">GetOverlaySurface</a>
</td>
<td align="left" width="63%">
Queries whether the caller should use the driver's overlay surface, and if so, returns a pointer to the surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-getvideoformats">GetVideoFormats</a>
</td>
<td align="left" width="63%">
Retrieves the video formats the driver supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-getvpdatainfo">GetVPDataInfo</a>
</td>
<td align="left" width="63%">
Retrieves the current video port data information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-informvpinputformats">InformVPInputFormats</a>
</td>
<td align="left" width="63%">
Informs the device what video formats the video port supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-setconnectinfo">SetConnectInfo</a>
</td>
<td align="left" width="63%">
Sets the video port connection parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-setddsurfacekernelhandles">SetDDSurfaceKernelHandles</a>
</td>
<td align="left" width="63%">
Specifies the kernel-mode handles of the DirectDraw surfaces to be used for the overlay suface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-setdirectdrawkernelhandle">SetDirectDrawKernelHandle</a>
</td>
<td align="left" width="63%">
Sets the kernel-mode handle to the DirectDraw object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-setinvertpolarity">SetInvertPolarity</a>
</td>
<td align="left" width="63%">
Reverses the current polarity the driver uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-setsurfaceparameters">SetSurfaceParameters</a>
</td>
<td align="left" width="63%">
Informs the device of the layout of the overlay surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-setvideoformat">SetVideoFormat</a>
</td>
<td align="left" width="63%">
Sets the video format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-setvideoportid">SetVideoPortID</a>
</td>
<td align="left" width="63%">
Specifies the ID of the hardware video port to use.

</td>
</tr>
</table> 


## -remarks



Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify</a>
 

 

