---
UID: NS:winsync._SYNC_VERSION
title: SYNC_VERSION (winsync.h)
description: Represents a version for an item or a change unit.
helpviewer_keywords: ["SYNC_VERSION","SYNC_VERSION structure [Windows Sync]","winsync.sync_version","winsync/SYNC_VERSION"]
old-location: winsync\sync_version.htm
tech.root: winsync
ms.assetid: 6a493a58-3dab-4032-90de-be9f903ae489
ms.date: 12/05/2018
ms.keywords: SYNC_VERSION, SYNC_VERSION structure [Windows Sync], winsync.sync_version, winsync/SYNC_VERSION
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
req.typenames: SYNC_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYNC_VERSION
 - winsync/_SYNC_VERSION
 - SYNC_VERSION
 - winsync/SYNC_VERSION
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
 - SYNC_VERSION
---

# SYNC_VERSION structure


## -description

Represents a version for an item or a change unit.

## -struct-fields

### -field dwLastUpdatingReplicaKey

The replica key that is associated with the version.

### -field ullTickCount

The tick count that is associated with the version.

## -remarks

A change that is made directly to a replica, such as a change that is made by a local application, will not have a version for the change in the synchronization metadata. A version that is created for such a change must contain the following elements:

<ul>
<li>The replica key of the local replica. This will typically be zero.</li>
<li>The current value of the tick count of the local replica.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumclockvector-next">IEnumClockVector::Next Method</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iforgottenknowledge-forgettoversion">IForgottenKnowledge::ForgetToVersion Method</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getchangeversion">ISyncChange::GetChangeVersion Method</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchange-getcreationversion">ISyncChange::GetCreationVersion Method</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase-additemmetadatatogroup">ISyncChangeBatchBase::AddItemMetadataToGroup Method</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebuilder-addchangeunitmetadata">ISyncChangeBuilder::AddChangeUnitMetadata Method</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangeunit-getchangeunitversion">ISyncChangeUnit::GetChangeUnitVersion Method</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-containschange">ISyncKnowledge::ContainsChange Method</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-containschangeunit">ISyncKnowledge::ContainsChangeUnit Method</a>



<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-convertversion">ISyncKnowledge::ConvertVersion Method</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-structures">Windows Sync Structures</a>