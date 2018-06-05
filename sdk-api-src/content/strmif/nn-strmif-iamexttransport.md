---
UID: NN:strmif.IAMExtTransport
title: IAMExtTransport
author: windows-sdk-content
description: The IAMExtTransport interface controls the transport on a video tape recporder (VTR) or camcorder.
old-location: dshow\iamexttransport.htm
old-project: DirectShow
ms.assetid: 4ce48038-bfcf-4b1f-8053-3446929a5f06
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMExtTransport, IAMExtTransport interface [DirectShow], IAMExtTransport interface [DirectShow],described, IAMExtTransportInterface, dshow.iamexttransport, strmif/IAMExtTransport
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMExtTransport
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport interface


## -description



The <b>IAMExtTransport</b> interface controls the transport on a video tape recporder (VTR) or camcorder. Applications can use this interface to play, record, or stop the transport; determine whether the transport contains media; and other transport-related functions. The implementation of this interface can vary, depending on the device. Some methods might return E_NOTIMPL if the device does not support them.

This interface also contains methods for non-linear editing through <i>edit events</i> and <i>edit property sets</i>. Currently, DirectShow does not provide any filters or drivers that implement this part of the interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMExtTransport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMExtTransport</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e0175b44-d1e6-4f3a-8aa7-893b41d0c487">get_AntiClogControl</a>
</td>
<td align="left" width="63%">
Determines if the anti-headclog control is enabled or disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83eb6f22-646c-400a-8adb-5545914656c9">get_EditStart</a>
</td>
<td align="left" width="63%">
Determines whether edit control is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/793078a2-bddd-469b-9043-f07830499353">get_LocalControl</a>
</td>
<td align="left" width="63%">
Retrieves the state of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/806356c7-796e-459f-8d5f-82c6b744bf07">get_MediaState</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee08cca0-a2ea-4a7c-8714-f22d5cd62fe8">get_Mode</a>
</td>
<td align="left" width="63%">
Retrieves the mode of the transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35a2fb2b-0963-4bdb-86a4-b5950b48a834">get_Rate</a>
</td>
<td align="left" width="63%">
Retrieves the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/340b7c9a-cfd9-4915-b0fc-0d12d7663578">GetBump</a>
</td>
<td align="left" width="63%">
Retrieves status of bump mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5544fd9-2899-4995-9401-a53f59d6400b">GetCapability</a>
</td>
<td align="left" width="63%">
Retrieves the general capabilities of an external transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ef12fa0-2ec9-45e5-9c22-20f810dac73b">GetChase</a>
</td>
<td align="left" width="63%">
Retrieves the status of chase mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c36b1fb1-f0a7-49df-8a6c-fb90ab268b23">GetEditProperty</a>
</td>
<td align="left" width="63%">
Retrieves individual parameters and values associated with a particular edit property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1afb45da-947c-454d-8be9-46ac58802b9e">GetEditPropertySet</a>
</td>
<td align="left" width="63%">
Retrieves the current state of an edit property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Determines the status of the transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90650920-f151-4e19-9133-4f1eb5eecbc2">GetTransportAudioParameters</a>
</td>
<td align="left" width="63%">
Retrieves the transport's audio parameter settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f670efe-4433-496d-b789-925c02b69f58">GetTransportBasicParameters</a>
</td>
<td align="left" width="63%">
Retrieves the transport's basic parameter settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a77ecf6-49e4-4d91-a06e-80313b4b8957">GetTransportVideoParameters</a>
</td>
<td align="left" width="63%">
Retrieves the transport's video parameter settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02d1e400-9959-4c68-ad8e-bc1700205179">put_AntiClogControl</a>
</td>
<td align="left" width="63%">
Enables or disables the transport's anti-headclog control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fd9c788-2ccb-47e5-bed8-fece9cfdf2a6">put_EditStart</a>
</td>
<td align="left" width="63%">
Activates edit control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ac75eb7-4b4c-402b-8e4e-f94488eccec1">put_LocalControl</a>
</td>
<td align="left" width="63%">
Sets the state of the device to local or remote control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5a4638e-3246-44dd-a7f8-52d0da12fc9c">put_MediaState</a>
</td>
<td align="left" width="63%">
Sets the current state of the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf941c07-6f42-4c63-9bdf-923f7a5b0b02">put_Mode</a>
</td>
<td align="left" width="63%">
Sets the movement of the transport to a new mode, such as play, stop, or record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/165966f1-f826-4ce2-b520-4a420898eee4">put_Rate</a>
</td>
<td align="left" width="63%">
Sets the playback rate for variable-speed external devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2f2b59f-2522-4f13-8861-fb4e2d9d406c">SetBump</a>
</td>
<td align="left" width="63%">
Temporarily changes the speed of playback for synchronization of multiple external devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8c94e74-e243-4fa9-85e6-8c027b514e4f">SetChase</a>
</td>
<td align="left" width="63%">
Enables or disables chase mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85ac14c7-7b47-4462-98ba-68a73f4c7497">SetEditProperty</a>
</td>
<td align="left" width="63%">
Defines individual parameters and values associated with a particular edit property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40695c7c-7381-44c0-b41f-7c838c9c83b5">SetEditPropertySet</a>
</td>
<td align="left" width="63%">
Registers an edit property set that describes a group of edit properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e013dd73-7276-48b3-bf5f-ffb4b3d49419">SetTransportAudioParameters</a>
</td>
<td align="left" width="63%">
Sets audio parameter settings for the transport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/798fa8d0-3834-4168-86a6-069cae3c3e8e">SetTransportBasicParameters</a>
</td>
<td align="left" width="63%">
Sets the transport's basic parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a63f921-0abb-417b-89c0-9dfb30ebbe57">SetTransportVideoParameters</a>
</td>
<td align="left" width="63%">
Sets the video parameters for the transport.

</td>
</tr>
</table> 


## -remarks



The DV device drivers require some additional constants that are defined in the header file Xprtdefs.h.

For Windows Driver Model (WDM) devices, the <a href="https://msdn.microsoft.com/97432b99-e89b-4d69-963d-a959f887e580">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567797">PROPSETID_EXT_TRANSPORT</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.

<h3><a id="Hardware_Requirements"></a><a id="hardware_requirements"></a><a id="HARDWARE_REQUIREMENTS"></a>Hardware Requirements</h3>
To control an external VCR, certain hardware requirements are recommended. VCRs with an RS-422 serial interface require a special serial port card or an external RS-232-to-RS-422 adapter. In addition, for best performance, your computer should have a serial port card built with a 16550 high-performance UART to sustain higher baud rates, such as 38.4 baud.

<h3><a id="Filter_Developers"></a><a id="filter_developers"></a><a id="FILTER_DEVELOPERS"></a>Filter Developers</h3>

           Implement this interface if you are writing a filter that controls an external device with a transport, such as a VTR. If you implement this interface, you should implement the <a href="https://msdn.microsoft.com/0423e888-39d1-45cb-9bcf-722240a31fbd">IAMExtDevice</a> interface as well.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

