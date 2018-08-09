---
UID: NS:traffic._TC_GEN_FLOW
title: "_TC_GEN_FLOW"
author: windows-sdk-content
description: The TC_GEN_FLOW structure creates a generic flow for use with the traffic control interface. The flow is customized through the members of this structure.
old-location: qos\tc_gen_flow.htm
old-project: qos
ms.assetid: 88b162d9-003c-42ce-8f82-91ee1aa9e32e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PTC_GEN_FLOW, PTC_GEN_FLOW, PTC_GEN_FLOW structure pointer [QOS], TC_GEN_FLOW, TC_GEN_FLOW structure [QOS], _TC_GEN_FLOW, _gqos_tc_gen_flow, qos.tc_gen_flow, traffic/PTC_GEN_FLOW, traffic/TC_GEN_FLOW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TC_GEN_FLOW, *PTC_GEN_FLOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Traffic.h
api_name:
 - TC_GEN_FLOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

