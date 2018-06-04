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

# IFaxOutboundRoutingGroup interface


## -description



		The <b>IFaxOutboundRoutingGroup</b> interface describes a configuration object that is used by a fax client application to retrieve information about an individual fax outbound routing group. The object also includes a method to retrieve the ordered collection of device IDs (<a href="https://msdn.microsoft.com/8ba11f07-3796-4910-98f7-541a32519c41">IFaxDeviceIds</a> interfaces) that participate in the routing group. The order of the devices in the collection determines the relative order in which available devices send outgoing transmissions.
		


## -remarks



A default implementation of <b>IFaxOutboundRoutingGroup</b> is provided as the <a href="https://msdn.microsoft.com/894a58b7-3a5f-4723-abcb-764567e49e76">FaxOutboundRoutingGroup</a> object.



