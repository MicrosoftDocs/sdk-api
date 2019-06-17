---
UID: NN:strmif.IAMExtTransport
title: IAMExtTransport (strmif.h)
author: windows-sdk-content
description: The IAMExtTransport interface controls the transport on a video tape recporder (VTR) or camcorder.
old-location: dshow\iamexttransport.htm
tech.root: DirectShow
ms.assetid: 4ce48038-bfcf-4b1f-8053-3446929a5f06
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMExtTransport, IAMExtTransport interface [DirectShow], IAMExtTransport interface [DirectShow],described, IAMExtTransportInterface, dshow.iamexttransport, strmif/IAMExtTransport
ms.topic: interface
f1_keywords: ["strmif/IAMExtTransport"]
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
 - IAMExtTransport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMExtTransport interface


## -description



The <b>IAMExtTransport</b> interface controls the transport on a video tape recporder (VTR) or camcorder. Applications can use this interface to play, record, or stop the transport; determine whether the transport contains media; and other transport-related functions. The implementation of this interface can vary, depending on the device. Some methods might return E_NOTIMPL if the device does not support them.

This interface also contains methods for non-linear editing through <i>edit events</i> and <i>edit property sets</i>. Currently, DirectShow does not provide any filters or drivers that implement this part of the interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMExtTransport</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMExtTransport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMExtTransport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_anticlogcontrol">get_AntiClogControl</a>
</td>
<td align="left" width="63%">
Determines if the anti-headclog control is enabled or disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_editstart">get_EditStart</a>
</td>
<td align="left" width="63%">
Determines whether edit control is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_localcontrol">get_LocalControl</a>
</td>
<td align="left" width="63%">
Retrieves the state of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_mediastate">get_MediaState</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_mode">get_Mode</a>
</td>
<td align="left" width="63%">
Retrieves the mode of the transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_rate">get_Rate</a>
</td>
<td align="left" width="63%">
Retrieves the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-getbump">GetBump</a>
</td>
<td align="left" width="63%">
Retrieves status of bump mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-getcapability">GetCapability</a>
</td>
<td align="left" width="63%">
Retrieves the general capabilities of an external transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-getchase">GetChase</a>
</td>
<td align="left" width="63%">
Retrieves the status of chase mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-geteditproperty">GetEditProperty</a>
</td>
<td align="left" width="63%">
Retrieves individual parameters and values associated with a particular edit property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-geteditpropertyset">GetEditPropertySet</a>
</td>
<td align="left" width="63%">
Retrieves the current state of an edit property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Determines the status of the transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-gettransportaudioparameters">GetTransportAudioParameters</a>
</td>
<td align="left" width="63%">
Retrieves the transport's audio parameter settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-gettransportbasicparameters">GetTransportBasicParameters</a>
</td>
<td align="left" width="63%">
Retrieves the transport's basic parameter settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-gettransportvideoparameters">GetTransportVideoParameters</a>
</td>
<td align="left" width="63%">
Retrieves the transport's video parameter settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_anticlogcontrol">put_AntiClogControl</a>
</td>
<td align="left" width="63%">
Enables or disables the transport's anti-headclog control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_editstart">put_EditStart</a>
</td>
<td align="left" width="63%">
Activates edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_localcontrol">put_LocalControl</a>
</td>
<td align="left" width="63%">
Sets the state of the device to local or remote control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_mediastate">put_MediaState</a>
</td>
<td align="left" width="63%">
Sets the current state of the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_mode">put_Mode</a>
</td>
<td align="left" width="63%">
Sets the movement of the transport to a new mode, such as play, stop, or record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_rate">put_Rate</a>
</td>
<td align="left" width="63%">
Sets the playback rate for variable-speed external devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-setbump">SetBump</a>
</td>
<td align="left" width="63%">
Temporarily changes the speed of playback for synchronization of multiple external devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-setchase">SetChase</a>
</td>
<td align="left" width="63%">
Enables or disables chase mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-seteditproperty">SetEditProperty</a>
</td>
<td align="left" width="63%">
Defines individual parameters and values associated with a particular edit property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-seteditpropertyset">SetEditPropertySet</a>
</td>
<td align="left" width="63%">
Registers an edit property set that describes a group of edit properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportaudioparameters">SetTransportAudioParameters</a>
</td>
<td align="left" width="63%">
Sets audio parameter settings for the transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportbasicparameters">SetTransportBasicParameters</a>
</td>
<td align="left" width="63%">
Sets the transport's basic parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportvideoparameters">SetTransportVideoParameters</a>
</td>
<td align="left" width="63%">
Sets the video parameters for the transport.

</td>
</tr>
</table> 


## -remarks



The DV device drivers require some additional constants that are defined in the header file Xprtdefs.h.

For Windows Driver Model (WDM) devices, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://docs.microsoft.com/windows-hardware/drivers/stream/propsetid-ext-transport">PROPSETID_EXT_TRANSPORT</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.

<h3><a id="Hardware_Requirements"></a><a id="hardware_requirements"></a><a id="HARDWARE_REQUIREMENTS"></a>Hardware Requirements</h3>
To control an external VCR, certain hardware requirements are recommended. VCRs with an RS-422 serial interface require a special serial port card or an external RS-232-to-RS-422 adapter. In addition, for best performance, your computer should have a serial port card built with a 16550 high-performance UART to sustain higher baud rates, such as 38.4 baud.

<h3><a id="Filter_Developers"></a><a id="filter_developers"></a><a id="FILTER_DEVELOPERS"></a>Filter Developers</h3>
Implement this interface if you are writing a filter that controls an external device with a transport, such as a VTR. If you implement this interface, you should implement the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamextdevice">IAMExtDevice</a> interface as well.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

