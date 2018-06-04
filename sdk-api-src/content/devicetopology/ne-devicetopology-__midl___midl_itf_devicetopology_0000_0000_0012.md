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

# __MIDL___MIDL_itf_devicetopology_0000_0000_0012 enumeration


## -description



The <b>PartType</b> enumeration defines constants that indicate whether a part in a device topology is a connector or subunit.




## -enum-fields




### -field Connector

The part is a connector. A connector can represent an audio jack, an internal connection to an integrated endpoint device, or a software connection implemented through DMA transfers. For more information about connector types, see <a href="https://msdn.microsoft.com/7171a880-2a3e-45aa-803d-26bf5e9e0365">ConnectorType Enumeration</a>.


### -field Subunit

The part is a subunit. A subunit is an audio-processing node in a device topology. A subunit frequently has one or more hardware control parameters that can be set under program control. For example, an audio application can change the volume setting of a volume-control subunit.


## -remarks



The <a href="https://msdn.microsoft.com/79af1dce-b946-4ef2-af36-4437603966da">IPart::GetPartType</a> method uses the constants defined in the <b>PartType</b> enumeration to indicate whether an <a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart</a> object represents a connector or a subunit. If an <b>IPart</b> object represents a connector, a client can query that that object for its <a href="https://msdn.microsoft.com/6eb5b439-3ac7-4c0b-84e2-b246c1b946a5">IConnector</a> interface. If an <b>IPart</b> object represents a subunit, a client can query that that object for its <a href="https://msdn.microsoft.com/9ec630bc-bba1-4a44-b66d-404a5221abbf">ISubunit</a> interface.

For more information about connectors and subunits, see <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>. 




## -see-also




<a href="https://msdn.microsoft.com/9dc9f182-3adf-4171-8829-35debae123da">Core Audio Constants</a>



<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>



<a href="https://msdn.microsoft.com/6eb5b439-3ac7-4c0b-84e2-b246c1b946a5">IConnector Interface</a>



<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>



<a href="https://msdn.microsoft.com/9ec630bc-bba1-4a44-b66d-404a5221abbf">ISubunit Interface</a>
 

 

