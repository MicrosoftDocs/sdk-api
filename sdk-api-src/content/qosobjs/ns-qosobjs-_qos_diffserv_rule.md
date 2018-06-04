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
 

 

