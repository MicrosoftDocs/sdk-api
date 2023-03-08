---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0004
title: SYNC_FULL_ENUMERATION_ACTION (winsync.h)
description: Represents the action to be taken by an application in response to ISyncCallback::OnFullEnumerationNeeded.
helpviewer_keywords: ["SFEA_ABORT","SFEA_FULL_ENUMERATION","SFEA_PARTIAL_SYNC","SYNC_FULL_ENUMERATION_ACTION","SYNC_FULL_ENUMERATION_ACTION enumeration [Windows Sync]","winsync.sync_full_enumeration_action","winsync/SFEA_ABORT","winsync/SFEA_FULL_ENUMERATION","winsync/SFEA_PARTIAL_SYNC","winsync/SYNC_FULL_ENUMERATION_ACTION"]
old-location: winsync\sync_full_enumeration_action.htm
tech.root: winsync
ms.assetid: 4fdb7123-d8c8-4ed7-9009-0e772252bbb7
ms.date: 12/05/2018
ms.keywords: SFEA_ABORT, SFEA_FULL_ENUMERATION, SFEA_PARTIAL_SYNC, SYNC_FULL_ENUMERATION_ACTION, SYNC_FULL_ENUMERATION_ACTION enumeration [Windows Sync], winsync.sync_full_enumeration_action, winsync/SFEA_ABORT, winsync/SFEA_FULL_ENUMERATION, winsync/SFEA_PARTIAL_SYNC, winsync/SYNC_FULL_ENUMERATION_ACTION
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
req.typenames: SYNC_FULL_ENUMERATION_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsync_0000_0000_0004
 - winsync/__MIDL___MIDL_itf_winsync_0000_0000_0004
 - SYNC_FULL_ENUMERATION_ACTION
 - winsync/SYNC_FULL_ENUMERATION_ACTION
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
 - SYNC_FULL_ENUMERATION_ACTION
---

# SYNC_FULL_ENUMERATION_ACTION enumeration


## -description

Represents the action to be taken by an application in response to <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback::OnFullEnumerationNeeded</a>.

## -enum-fields

### -field SFEA_FULL_ENUMERATION:0

Perform a full enumeration. This is the default option when the application does not register an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback</a> interface.

### -field SFEA_PARTIAL_SYNC

Perform a partial synchronization. When this option is specified, the learned knowledge is applied as single item exceptions.

### -field SFEA_ABORT

Cancel the synchronization session. All methods will return errors as if they were canceled.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onfullenumerationneeded">ISyncCallback::OnFullEnumerationNeeded</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-enumerations">Windows Sync Enumerations</a>
