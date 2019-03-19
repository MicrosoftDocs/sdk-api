---
UID: NS:qosobjs._QOS_DIFFSERV
title: QOS_DIFFSERV (qosobjs.h)
author: windows-sdk-content
description: The QOS_DIFFSERV traffic control object is used to specify filters for the packet scheduler when it operates in Differentiated Services Mode.
old-location: qos\qos_diffserv.htm
tech.root: QOS
ms.assetid: 3d1035dc-0e46-46f4-abb3-26100356b60d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPQOS_DIFFSERV, LPQOS_DIFFSERV, LPQOS_DIFFSERV structure pointer [QOS], QOS_DIFFSERV, QOS_DIFFSERV structure [QOS], _gqos_qos_diffserv, qos.qos_diffserv, qosobjs/LPQOS_DIFFSERV, qosobjs/QOS_DIFFSERV"
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
 - QOS_DIFFSERV
product: Windows
targetos: Windows
req.typenames: QOS_DIFFSERV, *LPQOS_DIFFSERV
req.redist: 
---

# QOS_DIFFSERV structure


## -description


The 
<b>QOS_DIFFSERV</b> traffic control object is used to specify filters for the packet scheduler when it operates in Differentiated Services Mode.


## -struct-fields




### -field ObjectHdr

The QOS object 
<b>QOS_OBJECT_HDR</b>. The object type for this traffic control object should be 
QOS_OBJECT_DIFFSERV.


### -field DSFieldCount

Number of Diffserv Rules in this object.


### -field DiffservRule

Array of 
<a href="https://msdn.microsoft.com/732cfbec-4175-4397-854f-0d2a930e11bc">QOS_DIFFSERV_RULE</a> structures.


## -remarks



The 
<b>QOS_DIFFSERV</b> object is used to specify the set of Diffserv rules that apply to the specified flow, all of which are specified in the <b>DiffservRule</b> member. Each Diffserv rule has an InboundDSField value, which signifies the DSCP on the Inbound packet. The Diffserv Rules also have OutboundDSCP and UserPriority values for conforming and nonconforming packets. These indicate the DSCP and 802.1p values that go out on the forwarded packet. Note that the DSCP or UserPriority mapping based on ServiceType or 
<b>QOS_DS_CLASS</b> or 
<b>QOS_TRAFFIC_CLASS</b> is not used in this mode.




## -see-also




<a href="https://msdn.microsoft.com/732cfbec-4175-4397-854f-0d2a930e11bc">QOS_DIFFSERV_RULE</a>



<a href="https://msdn.microsoft.com/56eca8ef-2b6e-4380-869c-bf1a4c8fdb1f">QOS_DS_CLASS</a>



<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>



<a href="https://msdn.microsoft.com/60c6492f-ddcf-401c-8121-2349b89eb223">QOS_TRAFFIC_CLASS</a>
 

 

