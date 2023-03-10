---
UID: NF:devicetopology.IConnector.GetType
title: IConnector::GetType (devicetopology.h)
description: The GetType method gets the type of this connector.
helpviewer_keywords: ["GetType","GetType method [Core Audio]","GetType method [Core Audio]","IConnector interface","IConnector interface [Core Audio]","GetType method","IConnector.GetType","IConnector::GetType","IConnectorGetType","coreaudio.iconnector_gettype","devicetopology/IConnector::GetType"]
old-location: coreaudio\iconnector_gettype.htm
tech.root: CoreAudio
ms.assetid: 0e50d371-0a2e-4004-9225-4a9da7c3f139
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Core Audio], GetType method [Core Audio],IConnector interface, IConnector interface [Core Audio],GetType method, IConnector.GetType, IConnector::GetType, IConnectorGetType, coreaudio.iconnector_gettype, devicetopology/IConnector::GetType
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
 - IConnector::GetType
 - devicetopology/IConnector::GetType
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
 - IConnector.GetType
---

# IConnector::GetType


## -description

The <b>GetType</b> method gets the type of this connector.

## -parameters

### -param pType [out]

Pointer to a variable into which the method writes the connector type. The connector type is one of the following <a href="/windows/win32/api/devicetopology/ne-devicetopology-connectortype">ConnectorType</a> enumeration constants:

Unknown_Connector

Physical_Internal

Physical_External

Software_IO

Software_Fixed

Network

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pType</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

A connector corresponds to a "pin" in kernel streaming (KS) terminology. The mapping of KS pins to connectors is as follows:

<ul>
<li>If the KS pin communication type is KSPIN_COMMUNICATION_SINK, KSPIN_COMMUNICATION_SOURCE, or KSPIN_COMMUNICATION_BOTH, then the connector type is Software_IO.</li>
<li>Else, if the pin is part of a physical connection between two KS filters (devices) in the same audio adapter or in different audio adapters, then the connector type is Software_Fixed.</li>
<li>Else, if the KS pin category is KSNODETYPE_SPEAKER, KSNODETYPE_MICROPHONE, KSNODETYPE_LINE_CONNECTOR, or KSNODETYPE_SPDIF_INTERFACE, the connector type is Physical_External.</li>
<li>Else, for a pin that does not meet any of the preceding criteria, the connector type is Physical_Internal.</li>
</ul>
For more information about KS pins, see the Windows DDK documentation.

For a code example that calls the <b>GetType</b> method, see the implementation of the SelectCaptureDevice function in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>