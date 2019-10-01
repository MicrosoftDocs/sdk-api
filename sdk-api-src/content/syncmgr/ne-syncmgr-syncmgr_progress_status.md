---
UID: NE:syncmgr.SYNCMGR_PROGRESS_STATUS
title: SYNCMGR_PROGRESS_STATUS (syncmgr.h)
author: windows-sdk-content
description: Specifies the current progress status of a synchronization process. Used by ISyncMgrSyncCallback::ReportProgress.
old-location: shell\SYNCMGR_PROGRESS_STATUS.htm
tech.root: shell
ms.assetid: 78622014-643e-4449-b937-a6122a06f470
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SYNCMGR_PROGRESS_STATUS, SYNCMGR_PROGRESS_STATUS enumeration [Windows Shell], SYNCMGR_PS_CANCELED, SYNCMGR_PS_DISCONNECTED, SYNCMGR_PS_FAILED, SYNCMGR_PS_MAX, SYNCMGR_PS_SUCCEEDED, SYNCMGR_PS_UPDATING, SYNCMGR_PS_UPDATING_INDETERMINATE, shell.SYNCMGR_PROGRESS_STATUS, shell_SYNCMGR_PROGRESS_STATUS, syncmgr/SYNCMGR_PROGRESS_STATUS, syncmgr/SYNCMGR_PS_CANCELED, syncmgr/SYNCMGR_PS_DISCONNECTED, syncmgr/SYNCMGR_PS_FAILED, syncmgr/SYNCMGR_PS_MAX, syncmgr/SYNCMGR_PS_SUCCEEDED, syncmgr/SYNCMGR_PS_UPDATING, syncmgr/SYNCMGR_PS_UPDATING_INDETERMINATE
ms.topic: enum
f1_keywords: 
 - "syncmgr/SYNCMGR_PROGRESS_STATUS"
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
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
 - Syncmgr.h
api_name:
 - SYNCMGR_PROGRESS_STATUS
targetos: Windows
req.typenames: SYNCMGR_PROGRESS_STATUS
req.redist: 
ms.custom: 19H1
---

# SYNCMGR_PROGRESS_STATUS enumeration


## -description


Specifies the current progress status of a synchronization process. Used by <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress">ISyncMgrSyncCallback::ReportProgress</a>.


## -enum-fields




### -field SYNCMGR_PS_UPDATING

The progress status is currently being updated by the handler.


### -field SYNCMGR_PS_UPDATING_INDETERMINATE

Ignore step parameters. The progress bar cycles from left to right on a timer internal to the sync folder. This is known as marquee mode.


### -field SYNCMGR_PS_SUCCEEDED

The synchronization is complete.


### -field SYNCMGR_PS_FAILED

Indicates something went wrong during the synchronization.


### -field SYNCMGR_PS_CANCELED

The user canceled the synchronization before it completed. Upon receipt of this value, Sync Center updates the UI and enables the option to restart the sync for that item.


### -field SYNCMGR_PS_DISCONNECTED

The device being synchronized was disconnected before the sync completed..


### -field SYNCMGR_PS_MAX

Used only to declare the largest valid value in this enumeration. Do not use with <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress">ISyncMgrSyncCallback::ReportProgress</a>.

