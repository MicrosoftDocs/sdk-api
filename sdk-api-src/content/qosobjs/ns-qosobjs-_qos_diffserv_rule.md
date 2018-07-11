---
UID: NS:qosobjs._QOS_DIFFSERV_RULE
title: "_QOS_DIFFSERV_RULE"
author: windows-sdk-content
description: The QOS_DIFFSERV_RULE structure is used in conjunction with the traffic control object QOS_DIFFSERV to provide Diffserv rules for a given flow.
old-location: qos\qos_diffserv_rule.htm
old-project: qos
ms.assetid: 732cfbec-4175-4397-854f-0d2a930e11bc
ms.author: windowssdkdev
ms.date: 03/26/2018
ms.keywords: "*LPQOS_DIFFSERV_RULE, LPQOS_DIFFSERV_RULE, LPQOS_DIFFSERV_RULE structure pointer [QOS], QOS_DIFFSERV_RULE, QOS_DIFFSERV_RULE structure [QOS], _QOS_DIFFSERV_RULE, _gqos_qos_diffserv_rule, qos.qos_diffserv_rule, qosobjs/LPQOS_DIFFSERV_RULE, qosobjs/QOS_DIFFSERV_RULE"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: QOS_DIFFSERV_RULE, *LPQOS_DIFFSERV_RULE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - QosObjs.h
api_name:
 - QOS_DIFFSERV_RULE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _QOS_DIFFSERV_RULE structure


## -description


The 
<b>QOS_DIFFSERV_RULE</b> structure is used in conjunction with the traffic control object 
<a href="https://msdn.microsoft.com/3d1035dc-0e46-46f4-abb3-26100356b60d">QOS_DIFFSERV</a> to provide Diffserv rules for a given flow.


## -struct-fields




### -field InboundDSField

Diffserv code point (DSCP) on the inbound packet. <b>InboundDSField</b> must be unique for the interface, otherwise the flow addition will fail. 




Valid range is 0x00 - 0x3F.


### -field ConformingOutboundDSField

Diffserv code point (DSCP) marked on all conforming packets on the flow. This member can be used to remark the packet before it is forwarded. 




Valid range is 0x00 - 0x3F.


### -field NonConformingOutboundDSField

Diffserv code point (DSCP) marked on all nonconforming packets on the flow. This member can be used to remark the packet before it is forwarded. 




Valid range is 0x00 - 0x3F.


### -field ConformingUserPriority

UserPriority value marked on all conforming packets on the flow. This member can be used to remark the packet before it is forwarded. 




Valid range is 0-7


### -field NonConformingUserPriority

UserPriority value marked on all nonconforming packets on the flow. This member can be used to remark the packet before it is forwarded. 




Valid range is 0-7


## -see-also




<a href="https://msdn.microsoft.com/3d1035dc-0e46-46f4-abb3-26100356b60d">QOS_DIFFSERV</a>
 

 

