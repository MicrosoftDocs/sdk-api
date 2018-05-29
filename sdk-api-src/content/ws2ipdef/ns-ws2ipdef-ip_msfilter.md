---
UID: NS:ws2ipdef.ip_msfilter
title: ip_msfilter
author: windows-sdk-content
description: The ip_msfilter structure provides multicast filtering parameters for IPv4 addresses.
old-location: winsock\ip_msfilter.htm
old-project: WinSock
ms.assetid: 8d9d515e-9369-4d71-9614-6cbeb5557a5d
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: "*PIP_MSFILTER, IP_MSFILTER, IP_MSFILTER [Winsock], IP_MSFILTER structure [Winsock], PIP_MSFILTER, PIP_MSFILTER structure pointer [Winsock], ip_msfilter, ip_msfilter structure [Winsock], winsock.ip_msfilter, ws2ipdef/PIP_MSFILTER, ws2ipdef/ip_msfilter, ws2tcpip/PIP_MSFILTER, ws2tcpip/ip_msfilter"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2ipdef.h
req.include-header: Ws2tcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IP_MSFILTER, *PIP_MSFILTER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ws2ipdef.h
-	Ws2tcpip.h
api_name:
-	IP_MSFILTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ip_msfilter structure


## -description


The <b>ip_msfilter</b> structure provides multicast filtering parameters for IPv4 addresses.


## -struct-fields




### -field imsf_multiaddr

The IPv4 address of the multicast group.


### -field imsf_interface

The local IPv4 address of the interface  or the interface index on which the multicast group should be filtered. This value is in network byte order. If this member specifies an IPv4 address of 0.0.0.0, the default IPv4 multicast interface is used.

 To use an interface index of 1 would be the same as an IP address of  0.0.0.1.  


### -field imsf_fmode

The multicast filter mode to be used. This parameter can be either MCAST_INCLUDE (value of 0) to include particular multicast sources, or MCAST_EXCLUDE (value of 1) to exclude traffic from  specified sources.

On Windows Server 2003 and Windows XP, these values are defined in the <i>Ws2tcpip.h</i> header file. 

On Windows Vista
   and later, these values are defined as enumeration values in the <a href="https://msdn.microsoft.com/7ca9cb9b-618a-4e73-9e2a-18e55e5c00c0">MULTICAST_MODE_TYPE</a> enumeration defined in the <i>Ws2ipdef.h</i> header file.


### -field imsf_numsrc

The number of sources in the <b>imsf_slist</b> member.


### -field imsf_slist

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a> structures that specify the IPv4 multicast source addresses to include or exclude.


## -remarks



The <b>ip_msfilter</b> structure is used with IPv4 addresses. The <b>ip_msfilter</b> structure is passed as an argument  for the <b>SIO_GET_MULTICAST_FILTER</b> and <b>SIO_SET_MULTICAST_FILTER</b> IOCTLs. 

The <b>ip_msfilter</b> structure and related structures used for IPv4 multicast programming are based on IETF recommendations in sections 4 and 8.1 of RFC 3768. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=87353">http://www.ietf.org/rfc/rfc3678.txt</a>.

On Windows Vista and later, a set of socket options are available for multicast programming that support IPv6 and IPv4 addresses. These socket options are IP agnostic and can be used on both IPv6 and IPv4. These IP agnostic options use the <a href="https://msdn.microsoft.com/053cf2c3-4f31-4f1e-be5c-d857e74d9465">GROUP_REQ</a> and the <a href="https://msdn.microsoft.com/c8f442e0-e7c3-4421-a664-3f4e31a68eb9">GROUP_SOURCE_REQ</a> structures and the <b>SIOCSMSFILTER</b>
and <b>SIOCGMSFILTER</b> IOCTLs. These are the preferred socket options and IOCTLs for multicast programming on Windows Vista and later.

The <b>imsf_interface</b> member can be an interface index. Any IPv4 address in the 0.x.x.x block (first octet of 0) except for the IPv4 address of 0.0.0.0 is treated as an interface index.
An interface index is a 24-bit number. The 0.0.0.0/8 IPv4 address block is not used (this range is reserved). The <a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a> function can be used to obtain interface index information to use for the <b>imsf_interface</b> member.

It is recommended that a local IPv4 address or interface index always be specified in the <b>imsf_interface</b> member of the <b>ip_msfilter</b> structure, rather than use the default interface.  This is particularly important on computers with multiple network interfaces and multiple public IPv4 addresses. 

The default interface used for IPv4 multicast is  determined by the networking stack in Windows. An application can determine the default interface used for IPv4 multicast using the <a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a> function to retrieve the IPv4 routing table. The network interface with the lowest value for the routing metric for a destination IP address of 224.0.0.0 is the default interface for IPv4 multicast. The routing table can also be displayed from the command prompt with the following command:

<b>route print</b>

The <a href="https://msdn.microsoft.com/6b06a29e-59cd-4446-bd2f-131dc25bf571">IP_MULTICAST_IF</a> socket option can be used to set the default interface to send IPv4 multicast packets. This socket option does not change the default interface used to receive IPv4 multicast packets.


A typical IPv4  multicast application would use the <a href="https://msdn.microsoft.com/6b06a29e-59cd-4446-bd2f-131dc25bf571">IP_ADD_MEMBERSHIP</a> socket option with the <a href="https://msdn.microsoft.com/0bcf4c17-679d-42fc-b77e-722ce955d01f">ip_mreq</a> structure or the <b>IP_ADD_SOURCE_MEMBERSHIP</b> socket option with the <a href="https://msdn.microsoft.com/237bc55f-0b24-4615-85af-30ae6ad163fd">ip_mreq_source</a> structure to join a multicast group and listen for multicast packets on a specific interface. The <b>IP_MULTICAST_IF</b> socket option would be used to set the interface to send IPv4 multicast packets to the multicast group. The most common scenario would be a multicast application that listens and sends on the same interface for a multicast group. Multiple sockets might be used by a multicast application with one  socket for listening and one or more sockets for sending. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>ip_msfilter</b> structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.

<div class="alert"><b>Note</b>  The <b>IP_MSFILTER</b> and <b>PIP_MSFILTER</b> derived structures are only defined on the Windows SDK released with Windows Vista and later. The <b>ip_msfilter</b> structure should be used on earlier versions of the Windows SDK. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/71c05393-3f8c-42c0-9060-e0df9b5e2578">Final-State-Based Multicast Programming</a>



<a href="https://msdn.microsoft.com/09aa1f67-c858-4bef-9a98-ce25ebcc1d4e">GROUP_FILTER</a>



<a href="https://msdn.microsoft.com/053cf2c3-4f31-4f1e-be5c-d857e74d9465">GROUP_REQ</a>



<a href="https://msdn.microsoft.com/c8f442e0-e7c3-4421-a664-3f4e31a68eb9">GROUP_SOURCE_REQ</a>



<a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a>



<a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a>



<a href="https://msdn.microsoft.com/6b06a29e-59cd-4446-bd2f-131dc25bf571">IPPROTO_IP Socket Options</a>



<a href="https://msdn.microsoft.com/7ca9cb9b-618a-4e73-9e2a-18e55e5c00c0">MULTICAST_MODE_TYPE</a>



<a href="https://msdn.microsoft.com/f729945b-b469-4baf-ac06-2431ee2d0e71">Multicast Programming</a>



<a href="https://msdn.microsoft.com/e2831f76-4499-45b6-bc60-2908ec3a246c">Socket Options</a>



<a href="https://msdn.microsoft.com/0bcf4c17-679d-42fc-b77e-722ce955d01f">ip_mreq</a>



<a href="https://msdn.microsoft.com/237bc55f-0b24-4615-85af-30ae6ad163fd">ip_mreq_source</a>
 

 

