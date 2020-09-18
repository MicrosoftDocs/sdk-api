---
UID: NS:winsync._SYNC_RANGE
title: SYNC_RANGE (winsync.h)
description: Represents a range of item IDs.
helpviewer_keywords: ["SYNC_RANGE","SYNC_RANGE structure [Windows Sync]","winsync.sync_range","winsync/SYNC_RANGE"]
old-location: winsync\sync_range.htm
tech.root: winsync
ms.assetid: d3e4a4f4-4a67-4dce-a81a-3861dcf788e6
ms.date: 12/05/2018
ms.keywords: SYNC_RANGE, SYNC_RANGE structure [Windows Sync], winsync.sync_range, winsync/SYNC_RANGE
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
req.typenames: SYNC_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYNC_RANGE
 - winsync/_SYNC_RANGE
 - SYNC_RANGE
 - winsync/SYNC_RANGE
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
 - SYNC_RANGE
---

# SYNC_RANGE structure


## -description

Represents a range of item IDs.

## -struct-fields

### -field pbClosedLowerBound

The closed lower bound of item IDs that are contained in the range.

### -field pbClosedUpperBound

The closed upper bound of item IDs that are contained in the range.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-processfullenumerationchangebatch">IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch Method</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-projectontochangeunit">ISyncKnowledge::ProjectOntoRange Method</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-structures">Windows Sync Structures</a>