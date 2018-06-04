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

# _MIB_IPADDRTABLE structure


## -description


The 
<b>MIB_IPADDRTABLE</b> structure contains a table of IPv4 address entries.


## -struct-fields




### -field dwNumEntries

The number of IPv4 address entries in the table.


### -field table

A pointer to a table of IPv4 address entries implemented as an array of 
<a href="https://msdn.microsoft.com/ed1777bd-4c02-43e0-9bbb-6bb02702e1a4">MIB_IPADDRROW</a> structures.


## -remarks



The <a href="https://msdn.microsoft.com/03bf5645-8237-4c78-a921-47315cab1c44">GetIpAddrTable</a> function retrieves the interface–to–IPv4 address mapping table on a local computer and returns this information in an <b>MIB_IPADDRTABLE</b> structure.

The <b>MIB_IPADDRTABLE</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="https://msdn.microsoft.com/ed1777bd-4c02-43e0-9bbb-6bb02702e1a4">MIB_IPADDRROW</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_IPADDRROW</b> array entries in the <b>table</b> member. Any access to a <b>MIB_IPADDRROW</b> array entry should assume  padding may exist. 



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <a href="https://msdn.microsoft.com/ed1777bd-4c02-43e0-9bbb-6bb02702e1a4">MIB_IPADDRROW</a> is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.



#### Examples

To view an example that retrieves the <b>MIB_IPADDRTABLE</b> structure and then prints out the <a href="https://msdn.microsoft.com/ed1777bd-4c02-43e0-9bbb-6bb02702e1a4">MIB_IPADDRROW</a> structures in this table, see the <a href="https://msdn.microsoft.com/03bf5645-8237-4c78-a921-47315cab1c44">GetIpAddrTable</a> function.

<div class="code"></div>



## -see-also




<a href="_iphlp_getipaddrtable">GetIpAddrTable</a>



<a href="https://msdn.microsoft.com/ed1777bd-4c02-43e0-9bbb-6bb02702e1a4">MIB_IPADDRROW</a>
 

 

