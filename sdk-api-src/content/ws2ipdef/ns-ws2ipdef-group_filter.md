---
UID: NS:ws2ipdef.group_filter
title: GROUP_FILTER
author: windows-sdk-content
description: Provides multicast filtering parameters for multicast IPv6 or IPv4 addresses.
old-location: winsock\group_filter.htm
tech.root: winsock
ms.assetid: 09aa1f67-c858-4bef-9a98-ce25ebcc1d4e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PGROUP_FILTER, GROUP_FILTER, GROUP_FILTER structure [Winsock], MCAST_EXCLUDE, MCAST_INCLUDE, PGROUP_FILTER, PGROUP_FILTER structure pointer [Winsock], winsock.group_filter, ws2ipdef/GROUP_FILTER, ws2ipdef/PGROUP_FILTER"
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
 - Ws2ipdef.h
api_name:
 - GROUP_FILTER
product: Windows
targetos: Windows
req.typenames: GROUP_FILTER, *PGROUP_FILTER
req.redist: 
---

# GROUP_FILTER structure


## -description


The <b>GROUP_FILTER</b> structure provides multicast filtering parameters for multicast IPv6 or IPv4 addresses.


## -struct-fields




### -field gf_interface

The interface index of the local interface for the multicast group to filter. 


### -field gf_group

The multicast address group that should be filtered. This may be either an IPv6 or IPv4 multicast address.


### -field gf_fmode

The multicast filter mode. 

This member can be one of the values from the <a href="https://msdn.microsoft.com/en-us/library/Bb427442(v=VS.85).aspx">MULTICAST_MODE_TYPE</a> enumeration type defined in the <i>Ws2ipdef.h</i> header file. This member determines if the list of IP addresses in the <b>gf_numsrc</b> member should be included or excluded.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MCAST_INCLUDE"></a><a id="mcast_include"></a><dl>
<dt><b>MCAST_INCLUDE</b></dt>
</dl>
</td>
<td width="60%">
The filter contains a list of IP addresses to include. 



</td>
</tr>
<tr>
<td width="40%"><a id="_MCAST_EXCLUDE"></a><a id="_mcast_exclude"></a><dl>
<dt><b> MCAST_EXCLUDE</b></dt>
</dl>
</td>
<td width="60%">
The filter contains a list of IP addresses to exclude. 

</td>
</tr>
</table>
 


### -field gf_numsrc

The number of multicast filter source address entries in the <b>gf_slist</b> member. 


### -field gf_slist

An array of <a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a> structures specifying the multicast source addresses to include or exclude. These IP addresses may be either IPv6 or IPv4 addresses, but they must be the same address family (IPv6 or IPv4) as the address specified in the <b>gf_group</b> member..


## -remarks



The <b>GROUP_FILTER</b> structure is used with either IPv6 or IPv4 multicast addresses. The <b>GROUP_FILTER</b> structure is passed as an argument  for the <b>SIOCGMSFILTER</b> and <b>SIOCSMSFILTER</b> IOCTLs.  

The <b>GROUP_FILTER</b> structure and related structures used for multicast programming are based on IETF recommendations in sections 5 and 8.2  of RFC 3768. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=87353">http://www.ietf.org/rfc/rfc3678.txt</a>.

On Windows Vista and later, a set of socket options are available for multicast programming that support IPv6 and IPv4 addresses. These socket options are IP agnostic and can be used on both IPv6 and IPv4. These IP agnostic options use the <a href="https://msdn.microsoft.com/053cf2c3-4f31-4f1e-be5c-d857e74d9465">GROUP_REQ</a> and the <a href="https://msdn.microsoft.com/c8f442e0-e7c3-4421-a664-3f4e31a68eb9">GROUP_SOURCE_REQ</a> structures and are the preferred socket options for multicast programming on Windows Vista and later.

The <a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a> function can be used to obtain interface index information required for the <i>gf_interface</i> member.

The <b>GROUP_FILTER</b> structure and the Ioctls that use this structure are only valid on datagram and raw sockets (the socket type must be <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>).

The <b>GROUP_FILTER</b> structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/053cf2c3-4f31-4f1e-be5c-d857e74d9465">GROUP_REQ</a>



<a href="https://msdn.microsoft.com/c8f442e0-e7c3-4421-a664-3f4e31a68eb9">GROUP_SOURCE_REQ</a>



<a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb427442(v=VS.85).aspx">MULTICAST_MODE_TYPE</a>



<a href="https://msdn.microsoft.com/f729945b-b469-4baf-ac06-2431ee2d0e71">Multicast Programming</a>



<a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a>



<a href="https://msdn.microsoft.com/e2831f76-4499-45b6-bc60-2908ec3a246c">Socket Options</a>



<a href="https://msdn.microsoft.com/0bcf4c17-679d-42fc-b77e-722ce955d01f">ip_mreq</a>



<a href="https://msdn.microsoft.com/8d9d515e-9369-4d71-9614-6cbeb5557a5d">ip_msfilter</a>



<a href="https://msdn.microsoft.com/672ce465-357c-450c-83a2-3cbdb28e018c">ipv6_mreq</a>
 

 

