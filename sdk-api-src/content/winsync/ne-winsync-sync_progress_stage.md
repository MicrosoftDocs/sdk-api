---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0003
title: SYNC_PROGRESS_STAGE (winsync.h)
description: Represents the stages of a synchronization session.
helpviewer_keywords: ["SPS_CHANGE_APPLICATION","SPS_CHANGE_DETECTION","SPS_CHANGE_ENUMERATION","SYNC_PROGRESS_STAGE","SYNC_PROGRESS_STAGE enumeration [Windows Sync]","winsync.sync_progress_stage","winsync/SPS_CHANGE_APPLICATION","winsync/SPS_CHANGE_DETECTION","winsync/SPS_CHANGE_ENUMERATION","winsync/SYNC_PROGRESS_STAGE"]
old-location: winsync\sync_progress_stage.htm
tech.root: winsync
ms.assetid: 06f8542a-d742-4cbb-bb44-c107b59ad38f
ms.date: 12/05/2018
ms.keywords: SPS_CHANGE_APPLICATION, SPS_CHANGE_DETECTION, SPS_CHANGE_ENUMERATION, SYNC_PROGRESS_STAGE, SYNC_PROGRESS_STAGE enumeration [Windows Sync], winsync.sync_progress_stage, winsync/SPS_CHANGE_APPLICATION, winsync/SPS_CHANGE_DETECTION, winsync/SPS_CHANGE_ENUMERATION, winsync/SYNC_PROGRESS_STAGE
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
req.typenames: SYNC_PROGRESS_STAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsync_0000_0000_0003
 - winsync/__MIDL___MIDL_itf_winsync_0000_0000_0003
 - SYNC_PROGRESS_STAGE
 - winsync/SYNC_PROGRESS_STAGE
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
 - SYNC_PROGRESS_STAGE
---

# SYNC_PROGRESS_STAGE enumeration


## -description

Represents the stages of a synchronization session.

## -enum-fields

### -field SPS_CHANGE_DETECTION:0

Changes are being detected on the source replica.

### -field SPS_CHANGE_ENUMERATION

Changes from the source replica are being enumerated.

### -field SPS_CHANGE_APPLICATION

Changes are being applied to the destination replica.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-enumerations">Windows Sync Enumerations</a>
