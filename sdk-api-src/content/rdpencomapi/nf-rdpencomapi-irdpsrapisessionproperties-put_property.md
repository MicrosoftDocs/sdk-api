---
UID: NF:rdpencomapi.IRDPSRAPISessionProperties.put_Property
title: IRDPSRAPISessionProperties::put_Property (rdpencomapi.h)
description: Sets or gets a named session property. (Put)
helpviewer_keywords: ["IRDPSRAPISessionProperties interface [RDP]","Property property","IRDPSRAPISessionProperties.Property","IRDPSRAPISessionProperties.put_Property","IRDPSRAPISessionProperties::Property","IRDPSRAPISessionProperties::get_Property","IRDPSRAPISessionProperties::put_Property","Property property [RDP]","Property property [RDP]","IRDPSRAPISessionProperties interface","Property property [RDP]","RDPSRAPISessionProperties object","RDPSRAPISessionProperties object [RDP]","Property property","put_Property","rdp.irdpsrapisessionproperties_property","rdpencomapi/IRDPSRAPISessionProperties::Property","rdpencomapi/IRDPSRAPISessionProperties::get_Property","rdpencomapi/IRDPSRAPISessionProperties::put_Property"]
old-location: rdp\irdpsrapisessionproperties_property.htm
tech.root: rdp
ms.assetid: 01aee262-95c0-4065-8f8c-e21db66f2a8c
ms.date: 12/05/2018
ms.keywords: IRDPSRAPISessionProperties interface [RDP],Property property, IRDPSRAPISessionProperties.Property, IRDPSRAPISessionProperties.put_Property, IRDPSRAPISessionProperties::Property, IRDPSRAPISessionProperties::get_Property, IRDPSRAPISessionProperties::put_Property, Property property [RDP], Property property [RDP],IRDPSRAPISessionProperties interface, Property property [RDP],RDPSRAPISessionProperties object, RDPSRAPISessionProperties object [RDP],Property property, put_Property, rdp.irdpsrapisessionproperties_property, rdpencomapi/IRDPSRAPISessionProperties::Property, rdpencomapi/IRDPSRAPISessionProperties::get_Property, rdpencomapi/IRDPSRAPISessionProperties::put_Property
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPISessionProperties::put_Property
 - rdpencomapi/IRDPSRAPISessionProperties::put_Property
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPISessionProperties.Property
 - IRDPSRAPISessionProperties.get_Property
 - IRDPSRAPISessionProperties.put_Property
 - RDPSRAPISessionProperties.Property
---

# IRDPSRAPISessionProperties::put_Property


## -description

Sets or gets a named session property.

This property is read/write.

## -parameters

## -remarks

You can set and get the following properties. The property names are case-sensitive.

<table>
<tr>
<th>Property name</th>
<th>Property description</th>
<th>Value type</th>
</tr>
<tr>
<td>
"DrvConAttach"

</td>
<td>
<div class="alert"><b>Note</b>  The <b>DrvConAttach</b> property is no longer available for use as of Windows 10. There is no longer a <i>mirror driver</i> for sharing.</div>
<div> </div>
There are two modes for the mirror driver attachment. The first is dynamic load mode. In this mode, the mirror driver will be attached immediately after an attendee is connected to the session and it has view control. The mirror driver will be automatically detached when the last attendee leaves the session (or there are no attendees with view control).

The second mode is static load mode. In this mode, the mirror driver is loaded immediately after the session is opened and is not unloaded until the session terminates. 

Note that in both modes the driver might be detached and re-attached as a result of external events like changing the screen resolution or sharing color depth.

Set this property to VARIANT_TRUE for dynamic attachment mode and to VARIANT_FALSE  for the static attachment mode.  Note that you can set this property only before calling the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-open">IRDPSRAPISharingSession::Open</a> method; this property becomes read-only after the <b>Open</b> method is called.   The default is VARIANT_TRUE.

For 1:1 scenarios such as Remote Assistance, you should use the dynamic load mode because it can take a very long time between the moment the session is opened and the moment an expert will connect.  

For 1:M (multiparty) scenarios, you should use the static load mode because attaching and detaching the mirror driver is quite disruptive and should not be done unless there is a good reason. 

</td>
<td>
<b>VT_BOOL</b>

</td>
</tr>
<tr>
<td>
"PortId"

</td>
<td>
Listener port for incoming connections from sharer. This property can be set on viewer side as well but will be used only for listening to connections in case of a reverse connect.

</td>
<td>
<b>VT_I4</b>

</td>
</tr>
<tr>
<td>
"PortProtocol"

</td>
<td>
Specifies the protocol family to start the listener on sharer. The possible values are as follows:



<dl>
<dt><a id="AF_UNSPEC"></a><a id="af_unspec"></a>AF_UNSPEC</dt>
<dd>
Value: 0

The address family is unspecified.

</dd>
<dt><a id="AF_INET"></a><a id="af_inet"></a>AF_INET</dt>
<dd>
Value: 2

The Internet Protocol version 4 (IPv4) address family.

</dd>
<dt><a id="AF_INET6"></a><a id="af_inet6"></a>AF_INET6</dt>
<dd>
Value: 23

The Internet Protocol version 6 (IPv6) address family.

</dd>
</dl>
</td>
<td>
<b>VT_I4</b>

</td>
</tr>
<tr>
<td>
"SetNetworkStream"

</td>
<td>
A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface that supports the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstream">IRDPSRAPITransportStream</a> interface. If this property is set, the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiviewer-connect">Connect</a> method will use this stream and ignore the connection string passed.

This property is valid for the viewer side only.

</td>
<td>
<b>VT_UNKNOWN</b>

</td>
</tr>
<tr>
<td>
"EnforceStrongEncryption"

</td>
<td>
If this property has a value of VARIANT_TRUE, the sharer requires the viewer to use Federal Information Processing Standard (FIPS) 140 compliant encryption. The default is VARIANT_FALSE.

This property becomes read-only after the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-open">IRDPSRAPISharingSession::Open</a> method is called. You can set this property only before calling that method. 

Viewer support for FIPS 140 compliance was added in Windows 10, version 1709. The sharer rejects connections from viewer versions previous to Windows 10, version 1709.

This property is valid for the sharer side only.

</td>
<td>
<b> VT_BOOL</b>

</td>
</tr>
<tr>
<td>
"FrameCaptureIntervalInMs"

</td>
<td>
Specifies the frame capture interval. By default, the frame capture interval is 33 milliseconds, which corresponds to 30 frames per second.

You can use this property to optimize performance. If screen updates do not need to be done so frequently, the capture interval can be increased. For example, a value of 400 milliseconds results in 2.5 frames per second.

This property is valid for the sharer side only.

</td>
<td>
<b>VT_I4</b>

</td>
</tr>
<tr>
<td>
"DefaultAttendeeControlLevel"

</td>
<td>
Specifies the default control level for attendees. By default, this value is CTRL_LEVEL_NONE (none). You can change this value to CTRL_LEVEL_VIEW (view). 

The default control level cannot be set to interactive.

This property is valid for the sharer side only.

</td>
<td>
<b>VT_I4</b>

</td>
</tr>
<tr>
<td>
"EnableClipboardRedirect"

</td>
<td>
If this property has a value of VARIANT_TRUE, the clipboard between sharer and viewer is activated. The default is VARIANT_FALSE.

To use clipboard sharing, the session must be in interactive mode.

Only a single connection can share the clipboard. The connection that most recently acquired input control takes over clipboard sharing. Clipboard sharing for any previous connection is automatically disabled. 

This property can only be used for desktop apps. 

This property is valid for the sharer side only.

This property is available starting with Windows 10, version 1511.

</td>
<td>
<b>VT_BOOL</b>

</td>
</tr>
<tr>
<td>
"SetClipboardRedirectCallback"

</td>
<td>
Specifies an IUnknown pointer to an instance of <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiclipboarduseevents">IRDPSRAPIClipboardUseEvents</a> that receives a callback each time a copying from the sharer computer to the viewer is attempted. This property is only relevant if clipboard sharing is enabled.

This property becomes read-only after the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-open">IRDPSRAPISharingSession::Open</a> method is called. You can set this property only before calling that method. 

This property can only be used for desktop apps. 

This property is valid for the sharer side only.

This property is available starting with Windows 10, version 1511.

</td>
<td>
<b>VT_UNKNOWN</b>

</td>
</tr>
<tr>
<td>
"EnabledTransports"

</td>
<td>
Specifies the transports to enable. A value of 3 supports both TCP and UDP. The default is 1, which is TCP only.

This property becomes read-only after the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-open">IRDPSRAPISharingSession::Open</a> method is called. You can set this property only before calling that method. 

This property is available starting with Windows 10, version 1803.

This property is valid for the sharer side only.

</td>
<td>
<b>VT_I4</b>

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisessionproperties">IRDPSRAPISessionProperties</a>
