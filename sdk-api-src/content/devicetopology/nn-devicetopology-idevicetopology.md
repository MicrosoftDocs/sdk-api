---
UID: NN:devicetopology.IDeviceTopology
title: IDeviceTopology
author: windows-driver-content
description: The IDeviceTopology interface provides access to the topology of an audio device.
old-location: coreaudio\idevicetopology.htm
old-project: CoreAudio
ms.assetid: 1b509f69-6277-40c0-a293-02afc30d464a
ms.author: windowsdriverdev
ms.date: 4/4/2018
ms.keywords: IDeviceTopology, IDeviceTopology interface [Core Audio], IDeviceTopology interface [Core Audio],described, coreaudio.idevicetopology, devicetopology/IDeviceTopology
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
req.typenames: ConnectorType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Devicetopology.h
api_name:
-	IDeviceTopology
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDeviceTopology interface


## -description



The <b>IDeviceTopology</b> interface provides access to the topology of an audio device. The topology of an audio <i>adapter</i> device consists of the data paths that lead to and from audio endpoint devices and the control points that lie along the paths. An audio <i>endpoint</i> device also has a topology, but it is trivial, as explained in <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>. A client obtains a reference to the <b>IDeviceTopology</b> interface for an audio endpoint device by following these steps:

<ol>
<li>By using one of the techniques described in <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>, obtain a reference to the <b>IMMDevice</b> interface for an audio endpoint device.</li>
<li>Call the <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a> method with parameter <i>refiid</i> set to <b>REFIID</b> IID_IDeviceTopology.</li>
</ol>
After obtaining the <b>IDeviceTopology</b> interface for an audio endpoint device, an application can explore the topologies of the audio adapter devices to which the endpoint device is connected.

For code examples that use the <b>IDeviceTopology</b> interface, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeviceTopology</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDeviceTopology</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a2da5d1e-ecd3-411e-8428-f529569cc11d">GetConnector</a>
</td>
<td align="left" width="63%">
Gets the connector that is specified by a connector number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b7f3b14-4c99-497b-a00e-a24535a621b7">GetConnectorCount</a>
</td>
<td align="left" width="63%">
Gets the number of connectors in the device-topology object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ecf8f23-7cfd-447a-ab76-8a23b79f5d6c">GetDeviceId</a>
</td>
<td align="left" width="63%">
Gets the device identifier of the device that is represented by the device-topology object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03310040-2081-47cf-88aa-6281c6bea56e">GetPartById</a>
</td>
<td align="left" width="63%">
Gets a part that is identified by its local ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f32ba6a-a82c-4c2c-8433-ebedd8799615">GetSignalPath</a>
</td>
<td align="left" width="63%">
Gets a list of parts in the signal path that links two parts, if the path exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6251cabd-9284-4311-bd5c-0c5b6d9a9be4">GetSubunit</a>
</td>
<td align="left" width="63%">
Gets the subunit that is specified by a subunit number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70fa57bb-56fe-4f8c-9967-10714f1cba22">GetSubunitCount</a>
</td>
<td align="left" width="63%">
Gets the number of subunits in the device topology.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a>
 

 

