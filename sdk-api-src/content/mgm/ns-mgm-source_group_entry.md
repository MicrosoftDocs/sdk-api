---
UID: NS:mgm._SOURCE_GROUP_ENTRY
title: SOURCE_GROUP_ENTRY (mgm.h)
description: The SOURCE_GROUP_ENTRY structure describes the entry returned by the group enumeration function MgmGroupEnumerationGetNext.
helpviewer_keywords: ["*PSOURCE_GROUP_ENTRY","PSOURCE_GROUP_ENTRY","PSOURCE_GROUP_ENTRY structure pointer [RAS]","SOURCE_GROUP_ENTRY","SOURCE_GROUP_ENTRY structure [RAS]","_mpr_source_group_entry_str","mgm/PSOURCE_GROUP_ENTRY","mgm/SOURCE_GROUP_ENTRY","rras.source_group_entry_str"]
old-location: rras\source_group_entry_str.htm
tech.root: RRAS
ms.assetid: 4964ccd9-e169-4afa-a9b3-1e4e4afb88c4
ms.date: 12/05/2018
ms.keywords: '*PSOURCE_GROUP_ENTRY, PSOURCE_GROUP_ENTRY, PSOURCE_GROUP_ENTRY structure pointer [RAS], SOURCE_GROUP_ENTRY, SOURCE_GROUP_ENTRY structure [RAS], _mpr_source_group_entry_str, mgm/PSOURCE_GROUP_ENTRY, mgm/SOURCE_GROUP_ENTRY, rras.source_group_entry_str'
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
targetos: Windows
req.typenames: SOURCE_GROUP_ENTRY, *PSOURCE_GROUP_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SOURCE_GROUP_ENTRY
 - mgm/_SOURCE_GROUP_ENTRY
 - PSOURCE_GROUP_ENTRY
 - mgm/PSOURCE_GROUP_ENTRY
 - SOURCE_GROUP_ENTRY
 - mgm/SOURCE_GROUP_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mgm.h
api_name:
 - SOURCE_GROUP_ENTRY
---

# SOURCE_GROUP_ENTRY structure


## -description

The 
<b>SOURCE_GROUP_ENTRY</b> structure describes the entry returned by the group enumeration function 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationgetnext">MgmGroupEnumerationGetNext</a>.

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

<a href="/windows/desktop/api/mgm/ne-mgm-mgm_enum_types">MGM_ENUM_TYPES</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationend">MgmGroupEnumerationEnd</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationgetnext">MgmGroupEnumerationGetNext</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationstart">MgmGroupEnumerationStart</a>