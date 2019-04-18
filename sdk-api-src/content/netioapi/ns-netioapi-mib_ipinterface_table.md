---
UID: NS:netioapi._MIB_IPINTERFACE_TABLE
title: MIB_IPINTERFACE_TABLE (netioapi.h)
author: windows-sdk-content
description: Contains a table of IP interface entries.
old-location: mib\mib_ipinterface_table.htm
tech.root: MIB
ms.assetid: c4bbb949-5573-42cd-bb03-e308ac40d569
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMIB_IPINTERFACE_TABLE, MIB_IPINTERFACE_TABLE, MIB_IPINTERFACE_TABLE structure [MIB], PMIB_IPINTERFACE_TABLE, PMIB_IPINTERFACE_TABLE structure pointer [MIB], _MIB_IPINTERFACE_TABLE, mib.mib_ipinterface_table, netioapi/MIB_IPINTERFACE_TABLE, netioapi/PMIB_IPINTERFACE_TABLE"
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
 - MIB_IPINTERFACE_TABLE
product: Windows
targetos: Windows
req.typenames: MIB_IPINTERFACE_TABLE, *PMIB_IPINTERFACE_TABLE
req.redist: 
ms.custom: 19H1
---

# MIB_IPINTERFACE_TABLE structure


## -description


The 
<b>MIB_IPINTERFACE_TABLE</b> structure contains a table of IP interface entries.


## -struct-fields




### -field NumEntries

The number of IP interface entries in the array.


### -field Table

An array of 
<a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> structures that contain IP interface entries.


## -remarks



The <b>MIB_IPINTERFACE_TABLE</b> structure is defined on Windows Vista and later. 

The <a href="https://msdn.microsoft.com/09f2bbff-3281-41ae-878f-61c5afa20ec5">GetIpInterfaceTable</a> function enumerates the IP interface entries on a local system and returns this information in a <b>MIB_IPINTERFACE_TABLE</b> structure. 



The <b>MIB_IPINTERFACE_TABLE</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_IPINTERFACE_ROW</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_IPINTERFACE_ROW</b> array entry should assume  padding may exist. 



Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.


#### Examples

To view an example that retrieves the <b>MIB_IPINTERFACE_TABLE</b> structure and then prints out a few members of the <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> structure entries in this table, see the <a href="https://msdn.microsoft.com/09f2bbff-3281-41ae-878f-61c5afa20ec5">GetIpInterfaceTable</a> function.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/09f2bbff-3281-41ae-878f-61c5afa20ec5">GetIpInterfaceTable</a>



<a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a>
 

 

