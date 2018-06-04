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

# _MIB_IPFORWARDTABLE structure


## -description


The 
<b>MIB_IPFORWARDTABLE</b> structure contains a table of IPv4 route entries.


## -struct-fields




### -field dwNumEntries

The number of route entries in the table.


### -field table

A pointer to a table of route entries implemented as an array of 
<a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a> structures.


## -remarks



The <a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a> function enumerates the IPv4 route entries on a local system and returns this information in a <b>MIB_IPFORWARDTABLE</b> structure. 



The <b>MIB_IPFORWARDTABLE</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_IPFORWARDROW</b> array entries in the <b>table</b> member. Any access to a <b>MIB_IPFORWARDROW</b> array entry should assume  padding may exist. 



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista
   and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.


#### Examples

To view an example that retrieves the <b>MIB_IPFORWARDTABLE</b> structure and then prints out the <a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a> structure entries in this table, see the <a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a> function.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a>



<a href="https://msdn.microsoft.com/71508d8e-3265-4c08-913c-248af2d8bbd6">MIB_IPFORWARDNUMBER</a>



<a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a>
 

 

