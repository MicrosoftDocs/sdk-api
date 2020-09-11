---
UID: NN:devicetopology.IDeviceTopology
title: IDeviceTopology (devicetopology.h)
description: The IDeviceTopology interface provides access to the topology of an audio device.
helpviewer_keywords: ["IDeviceTopology","IDeviceTopology interface [Core Audio]","IDeviceTopology interface [Core Audio]","described","coreaudio.idevicetopology","devicetopology/IDeviceTopology"]
old-location: coreaudio\idevicetopology.htm
tech.root: CoreAudio
ms.assetid: 1b509f69-6277-40c0-a293-02afc30d464a
ms.date: 12/05/2018
ms.keywords: IDeviceTopology, IDeviceTopology interface [Core Audio], IDeviceTopology interface [Core Audio],described, coreaudio.idevicetopology, devicetopology/IDeviceTopology
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeviceTopology
 - devicetopology/IDeviceTopology
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IDeviceTopology
---

# IDeviceTopology interface


## -description

The <b>IDeviceTopology</b> interface provides access to the topology of an audio device. The topology of an audio <i>adapter</i> device consists of the data paths that lead to and from audio endpoint devices and the control points that lie along the paths. An audio <i>endpoint</i> device also has a topology, but it is trivial, as explained in <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>. A client obtains a reference to the <b>IDeviceTopology</b> interface for an audio endpoint device by following these steps:

<ol>
<li>By using one of the techniques described in <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>, obtain a reference to the <b>IMMDevice</b> interface for an audio endpoint device.</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>refiid</i> set to <b>REFIID</b> IID_IDeviceTopology.</li>
</ol>
After obtaining the <b>IDeviceTopology</b> interface for an audio endpoint device, an application can explore the topologies of the audio adapter devices to which the endpoint device is connected.

For code examples that use the <b>IDeviceTopology</b> interface, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeviceTopology</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDeviceTopology</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDeviceTopology</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getconnector">GetConnector</a>
</td>
<td align="left" width="63%">
Gets the connector that is specified by a connector number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getconnectorcount">GetConnectorCount</a>
</td>
<td align="left" width="63%">
Gets the number of connectors in the device-topology object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getdeviceid">GetDeviceId</a>
</td>
<td align="left" width="63%">
Gets the device identifier of the device that is represented by the device-topology object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getpartbyid">GetPartById</a>
</td>
<td align="left" width="63%">
Gets a part that is identified by its local ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsignalpath">GetSignalPath</a>
</td>
<td align="left" width="63%">
Gets a list of parts in the signal path that links two parts, if the path exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsubunit">GetSubunit</a>
</td>
<td align="left" width="63%">
Gets the subunit that is specified by a subunit number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsubunitcount">GetSubunitCount</a>
</td>
<td align="left" width="63%">
Gets the number of subunits in the device topology.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>

