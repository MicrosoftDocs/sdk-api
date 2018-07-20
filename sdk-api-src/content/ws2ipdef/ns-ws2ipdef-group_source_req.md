---
UID: NS:ws2ipdef.group_source_req
title: group_source_req
author: windows-sdk-content
description: Provides multicast group information for IPv6 or IPv4 addresses that includes the source IP address.
old-location: winsock\group_source_req.htm
old-project: winsock
ms.assetid: c8f442e0-e7c3-4421-a664-3f4e31a68eb9
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*PGROUP_SOURCE_REQ, GROUP_SOURCE_REQ, GROUP_SOURCE_REQ structure [Winsock], PGROUP_SOURCE_REQ, PGROUP_SOURCE_REQ structure pointer [Winsock], group_source_req, winsock.group_source_req, ws2ipdef/GROUP_SOURCE_REQ, ws2ipdef/PGROUP_SOURCE_REQ"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2ipdef.h
req.include-header: Ws2tcpip.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GROUP_SOURCE_REQ, *PGROUP_SOURCE_REQ
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2ipdef.h
api_name:
 - GROUP_SOURCE_REQ
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# group_source_req structure


## -description


The <b>GROUP_SOURCE_REQ</b> structure provides multicast group information for IPv6 or IPv4 addresses that includes the source IP address.


## -struct-fields




### -field gsr_interface

The interface index of the local interface on which the multicast group should be joined, dropped, blocked, or unblocked. 


### -field gsr_group

The address of the multicast group. This may be either an IPv6 or IPv4 multicast address.


### -field gsr_source

The source address that should be used. This may be either an IPv6 or IPv4 multicast address, but it must be the same address family (IPv6 or IPv4) as the address specified in the <b>gsr_group</b> member.


## -remarks



The <b>GROUP_SOURCE_REQ</b> structure is used with either IPv6 or IPv4 multicast addresses. The <b>GROUP_SOURCE_REQ</b> structure is used with the <a href="https://msdn.microsoft.com/e2831f76-4499-45b6-bc60-2908ec3a246c">MCAST_BLOCK_SOURCE</a>,  MCAST_JOIN_SOURCE_GROUP, MCAST_LEAVE_SOURCE_GROUP, and MCAST_UNBLOCK_SOURCE socket options. 

The <b>GROUP_SOURCE_REQ</b> structure and related structures used for multicast programming are based on IETF recommendations in sections 5 and 8.2  of RFC 3768. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=87353">http://www.ietf.org/rfc/rfc3678.txt</a>.

On Windows Vista and later, a set of socket options are available for multicast programming that support IPv6 and IPv4 addresses. These socket options are IP agnostic and can be used on both IPv6 and IPv4. These IP agnostic options use the <a href="https://msdn.microsoft.com/053cf2c3-4f31-4f1e-be5c-d857e74d9465">GROUP_REQ</a> and the <b>GROUP_SOURCE_REQ</b> structures and are the preferred socket options for multicast programming on Windows Vista and later.

The <a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a> function can be used to obtain interface index information required for the <i>gsr_interface</i> member.

The <b>GROUP_SOURCE_REQ</b> structure and the socket options that use this structure are only valid on datagram and raw sockets (the socket type must be <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>).

The <b>GROUP_SOURCE_REQ</b> structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/09aa1f67-c858-4bef-9a98-ce25ebcc1d4e">GROUP_FILTER</a>



<a href="https://msdn.microsoft.com/053cf2c3-4f31-4f1e-be5c-d857e74d9465">GROUP_REQ</a>



<a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a>



<a href="https://msdn.microsoft.com/f729945b-b469-4baf-ac06-2431ee2d0e71">Multicast Programming</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a>



<a href="https://msdn.microsoft.com/e2831f76-4499-45b6-bc60-2908ec3a246c">Socket Options</a>



<a href="https://msdn.microsoft.com/0bcf4c17-679d-42fc-b77e-722ce955d01f">ip_mreq</a>



<a href="https://msdn.microsoft.com/672ce465-357c-450c-83a2-3cbdb28e018c">ipv6_mreq</a>
 

 

