---
UID: NN:devicetopology.IConnector
title: IConnector (devicetopology.h)
description: The IConnector interface represents a point of connection between components.
old-location: coreaudio\iconnector.htm
tech.root: CoreAudio
ms.assetid: 6eb5b439-3ac7-4c0b-84e2-b246c1b946a5
ms.date: 12/05/2018
ms.keywords: IConnector, IConnector interface [Core Audio], IConnector interface [Core Audio],described, coreaudio.iconnector, devicetopology/IConnector
ms.topic: interface
f1_keywords:
- devicetopology/IConnector
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
- IConnector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConnector interface


## -description



The <b>IConnector</b> interface represents a point of connection between components. The client obtains a reference to an <b>IConnector</b> interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getconnector">IDeviceTopology::GetConnector</a> or <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getconnectedto">IConnector::GetConnectedTo</a> method, or by calling the <b>IPart::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_IConnector.

An <b>IConnector</b> interface instance can represent:

<ul>
<li>An audio jack on a piece of hardware</li>
<li>An internal connection to an integrated endpoint device (for example, a built-in microphone in a laptop computer)</li>
<li>A software connection implemented through DMA transfers</li>
</ul>
The methods in the <b>IConnector</b> interface can describe various kinds of connectors. A connector has a type (a <a href="https://docs.microsoft.com/windows/win32/api/devicetopology/ne-devicetopology-connectortype">ConnectorType</a> enumeration constant) and a subtype (a GUID obtained from the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method).

A part in a device topology can be either a connector or a subunit. The <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface provides methods that are common to connectors and subunits.

For code examples that use the <b>IConnector</b> interface, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnector</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConnector</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-connectto">ConnectTo</a>
</td>
<td align="left" width="63%">
Connects this connector to a connector in another device-topology object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects this connector from another connector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getconnectedto">GetConnectedTo</a>
</td>
<td align="left" width="63%">
Gets the connector to which this connector is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getconnectoridconnectedto">GetConnectorIdConnectedTo</a>
</td>
<td align="left" width="63%">
Gets the global ID of the connector, if any, that this connector is connected to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getdataflow">GetDataFlow</a>
</td>
<td align="left" width="63%">
Gets the direction of data flow through this connector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto">GetDeviceIdConnectedTo</a>
</td>
<td align="left" width="63%">
Gets the device identifier of the audio device, if any, that this connector is connected to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-gettype">GetType</a>
</td>
<td align="left" width="63%">
Gets the type of this connector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-isconnected">IsConnected</a>
</td>
<td align="left" width="63%">
Indicates whether this connector is connected to another connector.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getconnectedto">IConnector::GetConnectedTo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getconnector">IDeviceTopology::GetConnector</a>
 

 

