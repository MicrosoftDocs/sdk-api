---
UID: NN:devicetopology.IConnector
title: IConnector
author: windows-sdk-content
description: The IConnector interface represents a point of connection between components.
old-location: coreaudio\iconnector.htm
tech.root: CoreAudio
ms.assetid: 6eb5b439-3ac7-4c0b-84e2-b246c1b946a5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IConnector, IConnector interface [Core Audio], IConnector interface [Core Audio],described, coreaudio.iconnector, devicetopology/IConnector
ms.prod: windows
ms.technology: windows-sdk
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
 - IConnector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConnector interface


## -description



The <b>IConnector</b> interface represents a point of connection between components. The client obtains a reference to an <b>IConnector</b> interface by calling the <a href="https://msdn.microsoft.com/a2da5d1e-ecd3-411e-8428-f529569cc11d">IDeviceTopology::GetConnector</a> or <a href="https://msdn.microsoft.com/bee0187c-5650-4b54-89b7-e63874048ed0">IConnector::GetConnectedTo</a> method, or by calling the <b>IPart::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_IConnector.

An <b>IConnector</b> interface instance can represent:

<ul>
<li>An audio jack on a piece of hardware</li>
<li>An internal connection to an integrated endpoint device (for example, a built-in microphone in a laptop computer)</li>
<li>A software connection implemented through DMA transfers</li>
</ul>
The methods in the <b>IConnector</b> interface can describe various kinds of connectors. A connector has a type (a <a href="https://msdn.microsoft.com/7171a880-2a3e-45aa-803d-26bf5e9e0365">ConnectorType</a> enumeration constant) and a subtype (a GUID obtained from the <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a> method).

A part in a device topology can be either a connector or a subunit. The <a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart</a> interface provides methods that are common to connectors and subunits.

For code examples that use the <b>IConnector</b> interface, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConnector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConnector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57704103-0124-4c02-8f96-980a50e98cca">ConnectTo</a>
</td>
<td align="left" width="63%">
Connects this connector to a connector in another device-topology object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1ca8863-4756-4d08-97b3-959a76d6f991">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects this connector from another connector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bee0187c-5650-4b54-89b7-e63874048ed0">GetConnectedTo</a>
</td>
<td align="left" width="63%">
Gets the connector to which this connector is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/865add93-9174-41c5-8998-b68f75eb35a1">GetConnectorIdConnectedTo</a>
</td>
<td align="left" width="63%">
Gets the global ID of the connector, if any, that this connector is connected to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55078775-2921-45c2-af27-c8ad53688293">GetDataFlow</a>
</td>
<td align="left" width="63%">
Gets the direction of data flow through this connector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f62bdeb-4765-467f-b68d-d94fc9a51dfb">GetDeviceIdConnectedTo</a>
</td>
<td align="left" width="63%">
Gets the device identifier of the audio device, if any, that this connector is connected to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e50d371-0a2e-4004-9225-4a9da7c3f139">GetType</a>
</td>
<td align="left" width="63%">
Gets the type of this connector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56aaee41-bf55-4556-b3d3-b0548a0db37c">IsConnected</a>
</td>
<td align="left" width="63%">
Indicates whether this connector is connected to another connector.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/bee0187c-5650-4b54-89b7-e63874048ed0">IConnector::GetConnectedTo</a>



<a href="https://msdn.microsoft.com/a2da5d1e-ecd3-411e-8428-f529569cc11d">IDeviceTopology::GetConnector</a>
 

 

