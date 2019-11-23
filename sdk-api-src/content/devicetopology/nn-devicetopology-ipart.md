---
UID: NN:devicetopology.IPart
title: IPart (devicetopology.h)

description: The IPart interface represents a part (connector or subunit) of a device topology.
old-location: coreaudio\ipart.htm
tech.root: CoreAudio
ms.assetid: 3bcfab9f-fad8-4605-8780-0b7c2068fcdf

ms.date: 12/05/2018
ms.keywords: IPart, IPart interface [Core Audio], IPart interface [Core Audio],described, coreaudio.ipart, devicetopology/IPart
ms.topic: interface
f1_keywords: 
 - "devicetopology/IPart"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPart interface


## -description



The <b>IPart</b> interface represents a part (connector or subunit) of a device topology. A client obtains a reference to an <b>IPart</b> interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getpartbyid">IDeviceTopology::GetPartById</a> or <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipartslist-getpart">IPartsList::GetPart</a> method, or by calling the <b>QueryInterface</b> method of the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector</a> or <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-isubunit">ISubunit</a> interface on a part object and setting the method's <i>iid</i> parameter to <b>REFIID</b> IID_IPart.

An object with an <b>IPart</b> interface can encapsulate one of the following device topology parts:

<ul>
<li><b>Connector.</b> This is a part that connects to another device to form a data path for transmitting an audio stream between devices.</li>
<li><b>Subunit.</b> This is a part that processes an audio stream (for example, volume control).</li>
</ul>
The <b>IPart</b> interface of a connector or subunit object represents the generic functions that are common to all parts, and the object's <b>IConnector</b> or <b>ISubunit</b> interface represents the functions that are specific to a connector or subunit. In addition, a part might support one or more control interfaces for controlling or monitoring the function of the part. For example, the client controls a volume-control subunit through its <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel</a> interface.

The <b>IPart</b> interface provides methods for getting the name, local ID, global ID, and part type of a connector or subunit. In addition, <b>IPart</b> can activate a control interface on a connector or subunit.

For code examples that use the <b>IPart</b> interface, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPart</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPart</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">Activate</a>
</td>
<td align="left" width="63%">
Activates an interface on a connector or subunit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-enumpartsincoming">EnumPartsIncoming</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the parts that reside on data paths that are upstream from this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-enumpartsoutgoing">EnumPartsOutgoing</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the parts that reside on data paths that are downstream from this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getcontrolinterface">GetControlInterface</a>
</td>
<td align="left" width="63%">
Gets a reference to the specified control interface, if this part supports it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount">GetControlInterfaceCount</a>
</td>
<td align="left" width="63%">
Gets the number of control interfaces that this part supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getglobalid">GetGlobalId</a>
</td>
<td align="left" width="63%">
Gets the global ID of this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getlocalid">GetLocalId</a>
</td>
<td align="left" width="63%">
Gets the local ID of this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the friendly name of this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getparttype">GetPartType</a>
</td>
<td align="left" width="63%">
Gets the part type of this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">GetSubType</a>
</td>
<td align="left" width="63%">
Gets the part subtype of this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-gettopologyobject">GetTopologyObject</a>
</td>
<td align="left" width="63%">
Gets a reference to the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology</a> interface of the device-topology object that contains this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-registercontrolchangecallback">RegisterControlChangeCallback</a>
</td>
<td align="left" width="63%">
Registers the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interface, which the client implements to receive notifications of status changes in this part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-unregistercontrolchangecallback">UnregisterControlChangeCallback</a>
</td>
<td align="left" width="63%">
Removes the registration of an <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interface that the client previously registered by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-registercontrolchangecallback">IPart::RegisterControlChangeCallback</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getpartbyid">IDeviceTopology::GetPartById</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipartslist-getpart">IPartsList::GetPart</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-isubunit">ISubunit Interface</a>
 

 

