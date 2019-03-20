---
UID: NS:qosobjs._QOS_TRAFFIC_CLASS
title: QOS_TRAFFIC_CLASS (qosobjs.h)
author: windows-sdk-content
description: The traffic control object QOS_TRAFFIC_CLASS is used to override the default UserPriority value ascribed to packets that classify the traffic of a given flow.
old-location: qos\qos_traffic_class.htm
tech.root: QOS
ms.assetid: 60c6492f-ddcf-401c-8121-2349b89eb223
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPQOS_TRAFFIC_CLASS, LPQOS_TRAFFIC_CLASS, LPQOS_TRAFFIC_CLASS structure pointer [QOS], QOS_TRAFFIC_CLASS, QOS_TRAFFIC_CLASS structure [QOS], SERVICETYPE_BESTEFFORT, SERVICETYPE_CONTROLLEDLOAD, SERVICETYPE_GUARANTEED, SERVICETYPE_NETWORK_CONTROL, SERVICETYPE_NONCONFORMING, SERVICETYPE_QUALITATIVE, _gqos_qos_traffic_class, qos.qos_traffic_class, qosobjs/LPQOS_TRAFFIC_CLASS, qosobjs/QOS_TRAFFIC_CLASS"
ms.topic: struct
req.header: qosobjs.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - QosObjs.h
api_name:
 - QOS_TRAFFIC_CLASS
product: Windows
targetos: Windows
req.typenames: QOS_TRAFFIC_CLASS, *LPQOS_TRAFFIC_CLASS
req.redist: 
---

# QOS_TRAFFIC_CLASS structure


## -description


The traffic control object 
<b>QOS_TRAFFIC_CLASS</b> is used to override the default UserPriority value ascribed to packets that classify the  traffic of a given flow. 

By default, the UserPriority value of a flow is derived from the ServiceType (see: <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>). Therefore, it is often necessary to override the default UserPriority because packets can be tagged in their Layer 2 headers (such as an 802.1p header) to specify their priority to Layer-2 devices. Using 
<b>QOS_TRAFFIC_CLASS</b> enables application developers to override the default UserPriority setting.


## -struct-fields




### -field ObjectHdr

The QOS object 
<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>. The object type for this traffic control object should be 
<b>QOS_OBJECT_TRAFFIC_CLASS</b>.


### -field TrafficClass

User priority value of the flow. The valid range is zero through seven. The following settings are chosen (by default) when the 
<b>QOS_TRAFFIC_CLASS</b> traffic control object is not used.

<div class="alert"><b>Note</b>  This parameter specifies an 802.1 TrafficClass parameter which has been provided to the host by a layer 2 network 
in an 802.1 extended RSVP RESV message. If this object is obtained
from the network, hosts will stamp the MAC headers of corresponding
transmitted packets, with the value in the object. Otherwise, hosts
can select a value based on the standard Intserv mapping of 
ServiceType to 802.1 TrafficClass.</div>
<div> </div>


#### SERVICETYPE_BESTEFFORT (0x00000001)



#### SERVICETYPE_CONTROLLEDLOAD (0x00000002)



#### SERVICETYPE_GUARANTEED (0x00000003)



#### SERVICETYPE_NONCONFORMING (0x00000009)



#### SERVICETYPE_NETWORK_CONTROL (0x0000000A)



#### SERVICETYPE_QUALITATIVE (0x0000000D)


## -remarks



<b>Traffic Control:  </b>The following <b>ServiceType</b> enumeration values are invalid when specifically working with Traffic Control. <dl>
<dd>SERVICE_NO_TRAFFIC_CONTROL</dd>
<dd>SERVICE_NO_QOS_SIGNALING</dd>
<dd>SERVICETYPE_GENERAL_INFORMATION</dd>
<dd>SERVICETYPE_NETWORK_UNAVAILABLE</dd>
<dd>SERVICETYPE_NOCHANGE</dd>
<dd>SERVICETYPE_NOTRAFFIC</dd>
</dl>





## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/3d1035dc-0e46-46f4-abb3-26100356b60d">QOS_DIFFSERV</a>



<a href="https://msdn.microsoft.com/732cfbec-4175-4397-854f-0d2a930e11bc">QOS_DIFFSERV_RULE</a>



<a href="https://msdn.microsoft.com/56eca8ef-2b6e-4380-869c-bf1a4c8fdb1f">QOS_DS_CLASS</a>



<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>
 

 

