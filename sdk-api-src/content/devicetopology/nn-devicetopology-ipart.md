---
UID: NN:devicetopology.IPart
title: IPart
author: windows-sdk-content
description: The IPart interface represents a part (connector or subunit) of a device topology.
old-location: coreaudio\ipart.htm
tech.root: CoreAudio
ms.assetid: 3bcfab9f-fad8-4605-8780-0b7c2068fcdf
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IPart, IPart interface [Core Audio], IPart interface [Core Audio],described, coreaudio.ipart, devicetopology/IPart
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: devicetopology.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IPart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPart interface


## -description



The <b>IPart</b> interface represents a part (connector or subunit) of a device topology. A client obtains a reference to an <b>IPart</b> interface by calling the <a href="https://msdn.microsoft.com/03310040-2081-47cf-88aa-6281c6bea56e">IDeviceTopology::GetPartById</a> or <a href="https://msdn.microsoft.com/505e2412-2849-4e64-9751-ce68831823b8">IPartsList::GetPart</a> method, or by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/6eb5b439-3ac7-4c0b-84e2-b246c1b946a5">IConnector</a> or <a href="https://msdn.microsoft.com/9ec630bc-bba1-4a44-b66d-404a5221abbf">ISubunit</a> interface on a part object and setting the method's <i>iid</i> parameter to <b>REFIID</b> IID_IPart.

An object with an <b>IPart</b> interface can encapsulate one of the following device topology parts:

<ul>
<li><b>Connector.</b> This is a part that connects to another device to form a data path for transmitting an audio stream between devices.</li>
<li><b>Subunit.</b> This is a part that processes an audio stream (for example, volume control).</li>
</ul>
The <b>IPart</b> interface of a connector or subunit object represents the generic functions that are common to all parts, and the object's <b>IConnector</b> or <b>ISubunit</b> interface represents the functions that are specific to a connector or subunit. In addition, a part might support one or more control interfaces for controlling or monitoring the function of the part. For example, the client controls a volume-control subunit through its <a href="https://msdn.microsoft.com/5e7d7111-e4b0-43b3-af35-9878d1a19e5f">IAudioVolumeLevel</a> interface.

The <b>IPart</b> interface provides methods for getting the name, local ID, global ID, and part type of a connector or subunit. In addition, <b>IPart</b> can activate a control interface on a connector or subunit.

For code examples that use the <b>IPart</b> interface, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPart</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPart</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPart</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">Activate</a>
</td>
<td align="left" width="63%">
Activates an interface on a connector or subunit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d74837e-12d1-4d94-941e-6a81aeac1151">EnumPartsIncoming</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the parts that reside on data paths that are upstream from this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1892e6d-a2d8-45c7-8a36-6040f4538c1e">EnumPartsOutgoing</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the parts that reside on data paths that are downstream from this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/802f3c19-5a71-41b0-922a-f216fd60495c">GetControlInterface</a>
</td>
<td align="left" width="63%">
Gets a reference to the specified control interface, if this part supports it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b82f69a-9b15-4bdf-9676-f2015ed67cfc">GetControlInterfaceCount</a>
</td>
<td align="left" width="63%">
Gets the number of control interfaces that this part supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07825373-3ab2-42d3-8c4b-4eaf2c45eb95">GetGlobalId</a>
</td>
<td align="left" width="63%">
Gets the global ID of this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5ca4908-1822-485c-a04a-0eeee1e384a8">GetLocalId</a>
</td>
<td align="left" width="63%">
Gets the local ID of this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a583f445-ebb2-4072-a272-6f186aef71b3">GetName</a>
</td>
<td align="left" width="63%">
Gets the friendly name of this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79af1dce-b946-4ef2-af36-4437603966da">GetPartType</a>
</td>
<td align="left" width="63%">
Gets the part type of this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">GetSubType</a>
</td>
<td align="left" width="63%">
Gets the part subtype of this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ad5fc66-6452-4d55-8c6a-a20a87431302">GetTopologyObject</a>
</td>
<td align="left" width="63%">
Gets a reference to the <a href="https://msdn.microsoft.com/1b509f69-6277-40c0-a293-02afc30d464a">IDeviceTopology</a> interface of the device-topology object that contains this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58cf52c9-20ee-46c4-926e-c374a4f42240">RegisterControlChangeCallback</a>
</td>
<td align="left" width="63%">
Registers the <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interface, which the client implements to receive notifications of status changes in this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3341421-6dab-43f3-87a8-83ee8a986a04">UnregisterControlChangeCallback</a>
</td>
<td align="left" width="63%">
Removes the registration of an <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interface that the client previously registered by a call to the <a href="https://msdn.microsoft.com/58cf52c9-20ee-46c4-926e-c374a4f42240">IPart::RegisterControlChangeCallback</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/5e7d7111-e4b0-43b3-af35-9878d1a19e5f">IAudioVolumeLevel Interface</a>



<a href="https://msdn.microsoft.com/6eb5b439-3ac7-4c0b-84e2-b246c1b946a5">IConnector Interface</a>



<a href="https://msdn.microsoft.com/03310040-2081-47cf-88aa-6281c6bea56e">IDeviceTopology::GetPartById</a>



<a href="https://msdn.microsoft.com/505e2412-2849-4e64-9751-ce68831823b8">IPartsList::GetPart</a>



<a href="https://msdn.microsoft.com/9ec630bc-bba1-4a44-b66d-404a5221abbf">ISubunit Interface</a>
 

 

