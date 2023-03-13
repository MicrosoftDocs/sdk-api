---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0008
title: FILTERING_TYPE (winsync.h)
description: Indicates the type of information that is included in a change batch during filtered synchronization.
helpviewer_keywords: ["FILTERING_TYPE","FILTERING_TYPE enumeration [Windows Sync]","FT_CURRENT_ITEMS_ONLY","winsync.filtering_type","winsync/FILTERING_TYPE","winsync/FT_CURRENT_ITEMS_ONLY"]
old-location: winsync\filtering_type.htm
tech.root: winsync
ms.assetid: 6bcbc011-9d47-4c88-a62e-0c9366abc7d3
ms.date: 12/05/2018
ms.keywords: FILTERING_TYPE, FILTERING_TYPE enumeration [Windows Sync], FT_CURRENT_ITEMS_ONLY, winsync.filtering_type, winsync/FILTERING_TYPE, winsync/FT_CURRENT_ITEMS_ONLY
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: FILTERING_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsync_0000_0000_0008
 - winsync/__MIDL___MIDL_itf_winsync_0000_0000_0008
 - FILTERING_TYPE
 - winsync/FILTERING_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsync.h
api_name:
 - FILTERING_TYPE
---

# FILTERING_TYPE enumeration


## -description

Indicates the type of information that is included in a change batch during filtered synchronization.

## -enum-fields

### -field FT_CURRENT_ITEMS_ONLY:0

The change batch includes data and metadata for items that are currently in the filter.

### -field FT_CURRENT_ITEMS_AND_VERSIONS_FOR_MOVED_OUT_ITEMS

## -remarks

A replica that does not keep ghosts for items that are not in the filter indicates this by using <b>FT_CURRENT_ITEMS_ONLY</b>.

<div class="alert"><b>Note</b>  An item that is excluded by the filter in one replica, but is still tracked in the other replica is known as a "ghost".</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-enumerations">Windows Sync Enumerations</a>
