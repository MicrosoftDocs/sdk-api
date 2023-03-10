---
UID: NN:devicetopology.IConnector
title: IConnector (devicetopology.h)
description: The IConnector interface represents a point of connection between components.
helpviewer_keywords: ["IConnector","IConnector interface [Core Audio]","IConnector interface [Core Audio]","described","coreaudio.iconnector","devicetopology/IConnector"]
old-location: coreaudio\iconnector.htm
tech.root: CoreAudio
ms.assetid: 6eb5b439-3ac7-4c0b-84e2-b246c1b946a5
ms.date: 12/05/2018
ms.keywords: IConnector, IConnector interface [Core Audio], IConnector interface [Core Audio],described, coreaudio.iconnector, devicetopology/IConnector
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
 - IConnector
 - devicetopology/IConnector
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
 - IConnector
---

# IConnector interface


## -description

The <b>IConnector</b> interface represents a point of connection between components. The client obtains a reference to an <b>IConnector</b> interface by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getconnector">IDeviceTopology::GetConnector</a> or <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getconnectedto">IConnector::GetConnectedTo</a> method, or by calling the <b>IPart::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_IConnector.

An <b>IConnector</b> interface instance can represent:

<ul>
<li>An audio jack on a piece of hardware</li>
<li>An internal connection to an integrated endpoint device (for example, a built-in microphone in a laptop computer)</li>
<li>A software connection implemented through DMA transfers</li>
</ul>
The methods in the <b>IConnector</b> interface can describe various kinds of connectors. A connector has a type (a <a href="/windows/win32/api/devicetopology/ne-devicetopology-connectortype">ConnectorType</a> enumeration constant) and a subtype (a GUID obtained from the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method).

A part in a device topology can be either a connector or a subunit. The <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface provides methods that are common to connectors and subunits.

For code examples that use the <b>IConnector</b> interface, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -inheritance

The <b>IConnector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConnector</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getconnectedto">IConnector::GetConnectedTo</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getconnector">IDeviceTopology::GetConnector</a>
