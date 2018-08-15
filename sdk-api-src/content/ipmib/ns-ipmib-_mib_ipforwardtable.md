---
UID: NS:ipmib._MIB_IPFORWARDTABLE
title: "_MIB_IPFORWARDTABLE"
author: windows-sdk-content
description: Contains a table of IPv4 route entries.
old-location: mib\mib_ipforwardtable.htm
old-project: mib
ms.assetid: bdecf944-fe19-4033-8778-362523984b03
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PMIB_IPFORWARDTABLE, MIB_IPFORWARDTABLE, MIB_IPFORWARDTABLE structure [MIB], PMIB_IPFORWARDTABLE, PMIB_IPFORWARDTABLE structure pointer [MIB], _MIB_IPFORWARDTABLE, _mpr_mib_ipforwardtable, ipmib/MIB_IPFORWARDTABLE, ipmib/PMIB_IPFORWARDTABLE, iprtrmib/MIB_IPFORWARDTABLE, iprtrmib/PMIB_IPFORWARDTABLE, mib.mib_ipforwardtable, rras.mib_ipforwardtable"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipmib.h
req.include-header: Iphlpapi.h
req.redist: 
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
req.typenames: MIB_IPFORWARDTABLE, *PMIB_IPFORWARDTABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipmib.h
 - Iprtrmib.h
api_name:
 - MIB_IPFORWARDTABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vistaand later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.


#### Examples

To view an example that retrieves the <b>MIB_IPFORWARDTABLE</b> structure and then prints out the <a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a> structure entries in this table, see the <a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a> function.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a>



<a href="https://msdn.microsoft.com/71508d8e-3265-4c08-913c-248af2d8bbd6">MIB_IPFORWARDNUMBER</a>



<a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a>
 

 

