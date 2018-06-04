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

# in_addr structure


## -description


The 
<b>in_addr</b> structure represents an IPv4 Internet address.


## -struct-fields




### -field S_un


### -field S_un.S_un_b

An IPv4 address formatted as four <b>u_char</b>s.


### -field S_un.S_un_b.s_b1

 


### -field S_un.S_un_b.s_b2

 


### -field S_un.S_un_b.s_b3

 


### -field S_un.S_un_b.s_b4

 


### -field S_un.S_un_w

An IPv4 address formatted as two <b>u_short</b>s.


### -field S_un.S_un_w.s_w1

 


### -field S_un.S_un_w.s_w2

 


### -field S_un.S_addr

An IPv4 address formatted as a <b>u_long</b>.


## -remarks



The <b>in_addr</b> structure is used with IPv4 addresses. 

The <b>in_addr</b> structure is the IPv4 equivalent of the IPv6-based <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">in6_addr</a> structure.  

<div class="alert"><b>Note</b>  The <b>IN_ADDR</b>, <b>PIN_ADDR</b>, and  <b>LPIN_ADDR</b> derived structures are only defined on the Windows SDK released with Windows Vista and later. The <b>IN_ADDR</b>, <b>PIN_ADDR</b>, and  <b>LPIN_ADDR</b> derived structures are defined in the <i>Inaddr.h</i> header file. On earlier versions of the Windows SDK, variables of this type should be declared as <b>struct in_addr</b>. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">in6_addr</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a>
 

 

