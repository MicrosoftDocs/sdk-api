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

# sockaddr_in6 structure


## -description


The SOCKADDR_IN6 structure specifies a transport address and port for the 
  <a href="https://msdn.microsoft.com/library/windows/hardware/ff543746">AF_INET6</a> address family.


## -struct-fields




### -field sin6_family

The address family for the transport address. This member should always be set to AF_INET6.


### -field sin6_port

A transport protocol port number.


### -field sin6_flowinfo

The IPv6 flow information.


### -field sin6_addr

An 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">IN6_ADDR</a> structure that contains an IPv6 transport
     address.


### -field sin6_scope_id

A ULONG representation of the IPv6 scope identifier that is defined in the 
      <b>sin6_scope_struct</b> member.


### -field sin6_scope_struct

A SCOPE_ID structure that contains the scope identifier for the IPv6 transport address. The
      SCOPE_ID structure is defined as follows:
      

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef struct {
  union {
    struct {
      ULONG  Zone : 28;
      ULONG  Level : 4;
    };
    ULONG  Value;
  };
} SCOPE_ID, *PSCOPE_ID;</pre>
</td>
</tr>
</table></span></div>




#### Zone

The zone index that identifies the zone to which the transport address pertains. Zones of the
        different scopes are instantiated as follows:
        

<ul>
<li>Each interface on a node comprises a single zone of interface-local scope.</li>
</ul>
<ul>
<li>Each link, and the interfaces attached to that link, comprise a single zone of link-local
         scope.</li>
</ul>
<ul>
<li>There is a single zone of global scope that comprises all of the links and interfaces in the
         Internet.</li>
</ul>
<ul>
<li>The boundaries of zones of scope other than interface-local, link-local, and global are
         defined by network administrators.</li>
</ul>
A value of zero specifies the default zone.



#### Level

The scope of the IPv6 transport address. This scope must be the same as the IPv6 scope value
        that is embedded in the IPv6 transport address. This member can be one of the following:
        

<b>ScopeLevelInterface</b>

The transport address has interface-local scope.

<b>ScopeLevelLink</b>

The transport address has link-local scope.

<b>ScopeLevelSubnet</b>

The transport address has subnet-local scope.

<b>ScopeLevelAdmin</b>

The transport address has admin-local scope.

<b>ScopeLevelSite</b>

The transport address has site-local scope.

<b>ScopeLevelOrganization</b>

The transport address has organization-local scope.

<b>ScopeLevelGlobal</b>

The transport address has global scope.



#### Value

A ULONG representation of the IPv6 scope identifier.


## -remarks



All of the data in the SOCKADDR_IN6 structure, except for the address family, must be specified in
    network-byte-order (big-endian).

The size of the SOCKADDR_IN6 structure is too large to fit in the memory space that is provided by a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a> structure. For a structure that is
    guaranteed to be large enough to contain a transport address for all possible address families, see 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543746">AF_INET6</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">IN6_ADDR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a>
 

 

