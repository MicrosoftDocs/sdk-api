---
UID: NS:netioapi._MIB_IF_TABLE2
title: "_MIB_IF_TABLE2"
author: windows-sdk-content
description: Contains a table of logical and physical interface entries.
old-location: mib\mib_if_table2.htm
tech.root: MIB
ms.assetid: 334078c6-afd0-4c53-838c-28bc3e1e8484
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PMIB_IF_TABLE2, MIB_IF_TABLE2, MIB_IF_TABLE2 structure [MIB], PMIB_IF_TABLE2, PMIB_IF_TABLE2 structure pointer [MIB], _MIB_IF_TABLE2, mib.mib_if_table2, netioapi/MIB_IF_TABLE2, netioapi/PMIB_IF_TABLE2"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - Netioapi.h
api_name:
 - MIB_IF_TABLE2
product: Windows
targetos: Windows
req.typenames: MIB_IF_TABLE2, *PMIB_IF_TABLE2
req.redist: 
---

# _MIB_IF_TABLE2 structure


## -description


The 
<b>MIB_IF_TABLE2</b> structure contains a table of logical and physical interface entries.


## -struct-fields




### -field NumEntries

The number of interface entries in the array.


### -field Table

An array of 
<a href="https://msdn.microsoft.com/e8bb79f9-e7e9-470b-8883-36d08061661b">MIB_IF_ROW2</a> structures containing interface entries.


## -remarks



The <b>MIB_IF_TABLE2</b> structure is defined in Windows Vista and later. 

The <a href="https://msdn.microsoft.com/0153c41c-b02b-4832-87b3-88dc3a9f4ff1">GetIfTable2</a> and <a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a> functions enumerates the logical and physical interfaces on a local system and returns this information in a <b>MIB_IF_TABLE2</b> structure. 



The <b>MIB_IF_TABLE2</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/e8bb79f9-e7e9-470b-8883-36d08061661b">MIB_IF_ROW2</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_IF_ROW2</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_IF_ROW2</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/0153c41c-b02b-4832-87b3-88dc3a9f4ff1">GetIfTable2</a>



<a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/e8bb79f9-e7e9-470b-8883-36d08061661b">MIB_IF_ROW2</a>
 

 

