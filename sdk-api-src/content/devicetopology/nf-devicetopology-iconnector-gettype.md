---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IConnector::GetType


## -description



The <b>GetType</b> method gets the type of this connector.




## -parameters




### -param pType [out]

Pointer to a variable into which the method writes the connector type. The connector type is one of the following <a href="https://msdn.microsoft.com/7171a880-2a3e-45aa-803d-26bf5e9e0365">ConnectorType</a> enumeration constants:

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

For a code example that calls the <b>GetType</b> method, see the implementation of the SelectCaptureDevice function in <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>.




## -see-also




<a href="https://msdn.microsoft.com/6eb5b439-3ac7-4c0b-84e2-b246c1b946a5">IConnector Interface</a>
 

 

