---
UID: NS:mgm._SOURCE_GROUP_ENTRY
title: SOURCE_GROUP_ENTRY
author: windows-sdk-content
description: The SOURCE_GROUP_ENTRY structure describes the entry returned by the group enumeration function MgmGroupEnumerationGetNext.
old-location: rras\source_group_entry_str.htm
tech.root: rras
ms.assetid: 4964ccd9-e169-4afa-a9b3-1e4e4afb88c4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSOURCE_GROUP_ENTRY, PSOURCE_GROUP_ENTRY, PSOURCE_GROUP_ENTRY structure pointer [RAS], SOURCE_GROUP_ENTRY, SOURCE_GROUP_ENTRY structure [RAS], _mpr_source_group_entry_str, mgm/PSOURCE_GROUP_ENTRY, mgm/SOURCE_GROUP_ENTRY, rras.source_group_entry_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mgm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mgm.h
api_name:
 - SOURCE_GROUP_ENTRY
product: Windows
targetos: Windows
req.typenames: SOURCE_GROUP_ENTRY, *PSOURCE_GROUP_ENTRY
req.redist: 
---

# SOURCE_GROUP_ENTRY structure


## -description


The 
<b>SOURCE_GROUP_ENTRY</b> structure describes the entry returned by the group enumeration function 
<a href="https://msdn.microsoft.com/a5e659e9-b566-490b-831b-96f9de822ebf">MgmGroupEnumerationGetNext</a>.


## -struct-fields




### -field dwSourceAddr

Specifies the source address from which to receive multicast data. Specify zero to receive data from all sources (a wildcard receiver for a group); otherwise, specify the IP address of the source or source network. 




To specify a range of source addresses, specify the source network using <b>dwSourceAddr</b>, and specify a subnet mask using <b>dwSourceMask</b>.


### -field dwSourceMask

Specifies the subnet mask that corresponds to <b>dwSourceAddr</b>. The <b>dwSourceAddr</b> and <b>dwSourceMask</b> parameters are used together to define a range of sources from which to receive multicast data. 




Specify zero for this parameter if zero was specified for <b>dwSourceAddr</b> (a wildcard receiver).
						


### -field dwGroupAddr

Specifies the multicast group for which to receive data. Specify zero to receive all groups (a wildcard receiver); otherwise, specify the IP address of the group. 




To specify a range of group addresses, specify the group address using <b>dwGroupAddr</b>, and specify a subnet mask using <b>dwGroupMask</b>.


### -field dwGroupMask

Specifies the subnet mask that corresponds to <b>dwGroupAddr</b>. The <b>dwGroupAddr</b> and <b>dwGroupMask</b> parameters are used together to define a range of multicast groups. 




Specify zero for this parameter if zero was specified for <b>dwGroupAddr</b> (a wildcard receiver).


## -see-also




<a href="https://msdn.microsoft.com/09b60342-25a8-4d0a-8176-3701f0622aa8">MGM_ENUM_TYPES</a>



<a href="https://msdn.microsoft.com/87a0bd96-c877-443e-a539-a31ab0971869">MgmGroupEnumerationEnd</a>



<a href="https://msdn.microsoft.com/a5e659e9-b566-490b-831b-96f9de822ebf">MgmGroupEnumerationGetNext</a>



<a href="https://msdn.microsoft.com/926f4055-becb-4c99-afd2-2d2822626f24">MgmGroupEnumerationStart</a>
 

 

