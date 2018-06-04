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

# IPAddrEntry structure


## -description


<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

Implements part of the Management Information Base (MIB-II) 
			information group for the Internet Protocol (IP) as specified in the 
			Internet Engineering Task Force (IETF) Request for Comments <a href="Http://go.microsoft.com/fwlink/p/?linkid=85308">(RFC) 2011</a>.


## -struct-fields




### -field iae_addr

An IPv4 IP address to which this structure pertains.


### -field iae_index

The index value that uniquely identifies the interface associated with this
					IP address.


### -field iae_mask

The subnet mask associated with this IP address. The value of the mask is an 
					IPv4 address with all the network bits set to 1 and all the hosts bits set to 0.


### -field iae_bcastaddr

The value of the least-significant bit in the IP broadcast address used for 
					sending datagrams on the logical interface associated with this IP address. 
					For example, when the Internet standard all-ones broadcast address 
					is used, the value is 1. This value applies to both the subnet and network 
					broadcast addresses used by the entity on this logical interface.


### -field iae_reasmsize

The size of the largest IP datagram that this entity can reassemble from 
					incoming IP fragmented datagrams received on this interface.


### -field iae_context

A context value for this IP address.


### -field iae_pad

A pad value.


## -see-also




<a href="https://msdn.microsoft.com/b992b585-e1c8-4262-a6e0-ad8b5047620f">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/566bf187-73d0-4d61-be8e-306dc482a005">Management Information Base
			 Reference</a>
 

 

