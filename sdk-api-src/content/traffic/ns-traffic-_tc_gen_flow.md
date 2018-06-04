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

# _TC_GEN_FLOW structure


## -description


The 
<b>TC_GEN_FLOW</b> structure creates a generic flow for use with the traffic control interface. The flow is customized through the members of this structure.


## -struct-fields




### -field SendingFlowspec


<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure for the sending direction of the flow.


### -field ReceivingFlowspec


<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure for the receiving direction of the flow.


### -field TcObjectsLength

Length of <b>TcObjects</b>, in bytes.


### -field TcObjects

Buffer that contains an array of traffic control objects specific to the given flow. The <b>TcObjects</b> member can contain objects from the list of currently supported objects. Definitions of these objects can be found in Qos.h and Traffic.h: 





<a href="https://msdn.microsoft.com/56eca8ef-2b6e-4380-869c-bf1a4c8fdb1f">QOS_DS_CLASS</a>



<a href="https://msdn.microsoft.com/60c6492f-ddcf-401c-8121-2349b89eb223">QOS_TRAFFIC_CLASS</a>



<a href="https://msdn.microsoft.com/3d1035dc-0e46-46f4-abb3-26100356b60d">QOS_DIFFSERV</a>



<a href="https://msdn.microsoft.com/a1ae9920-3e6f-4611-abce-905df7a516f5">QOS_SD_MODE</a>



<a href="https://msdn.microsoft.com/2be833dc-d9e1-495d-831e-09c900c8adb2">QOS_SHAPING_RATE</a>


QOS_OBJECT_END_OF_LIST
						


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/3d1035dc-0e46-46f4-abb3-26100356b60d">QOS_DIFFSERV</a>



<a href="https://msdn.microsoft.com/56eca8ef-2b6e-4380-869c-bf1a4c8fdb1f">QOS_DS_CLASS</a>



<a href="https://msdn.microsoft.com/a1ae9920-3e6f-4611-abce-905df7a516f5">QOS_SD_MODE</a>



<a href="https://msdn.microsoft.com/2be833dc-d9e1-495d-831e-09c900c8adb2">QOS_SHAPING_RATE</a>



<a href="https://msdn.microsoft.com/60c6492f-ddcf-401c-8121-2349b89eb223">QOS_TRAFFIC_CLASS</a>
 

 

