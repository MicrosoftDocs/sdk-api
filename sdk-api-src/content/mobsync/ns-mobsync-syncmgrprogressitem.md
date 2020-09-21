---
UID: NS:mobsync._tagSYNCMGRPROGRESSITEM
title: SYNCMGRPROGRESSITEM (mobsync.h)
description: Provides status information while a synchronization is in progress. This structure is used with the ISyncMgrSynchronizeCallback::Progress method and corresponds to a single synchronization item.
helpviewer_keywords: ["*LPSYNCMGRPROGRESSITEM","LPSYNCMGRPROGRESSITEM","LPSYNCMGRPROGRESSITEM structure pointer [Windows Shell]","SYNCMGRPROGRESSITEM","SYNCMGRPROGRESSITEM structure [Windows Shell]","mobsync/LPSYNCMGRPROGRESSITEM","mobsync/SYNCMGRPROGRESSITEM","shell.syncmgr_syncmgrprogressitem","syncmgr.syncmgrprogressitem"]
old-location: shell\syncmgr_syncmgrprogressitem.htm
tech.root: shell
ms.assetid: 94ac1206-be5f-467c-ab4a-11f574c406ca
ms.date: 12/05/2018
ms.keywords: '*LPSYNCMGRPROGRESSITEM, LPSYNCMGRPROGRESSITEM, LPSYNCMGRPROGRESSITEM structure pointer [Windows Shell], SYNCMGRPROGRESSITEM, SYNCMGRPROGRESSITEM structure [Windows Shell], mobsync/LPSYNCMGRPROGRESSITEM, mobsync/SYNCMGRPROGRESSITEM, shell.syncmgr_syncmgrprogressitem, syncmgr.syncmgrprogressitem'
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: SYNCMGRPROGRESSITEM, *LPSYNCMGRPROGRESSITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSYNCMGRPROGRESSITEM
 - mobsync/_tagSYNCMGRPROGRESSITEM
 - LPSYNCMGRPROGRESSITEM
 - mobsync/LPSYNCMGRPROGRESSITEM
 - SYNCMGRPROGRESSITEM
 - mobsync/SYNCMGRPROGRESSITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mobsync.h
api_name:
 - SYNCMGRPROGRESSITEM
---

# SYNCMGRPROGRESSITEM structure


## -description

Provides status information while a synchronization is in progress. This structure is used with the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress">ISyncMgrSynchronizeCallback::Progress</a> method and corresponds to a single synchronization item.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes.

### -field mask

Type: <b>UINT</b>

Flags from the <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrstatus">SYNCMGRSTATUS</a> enumeration that specify which members of this structure are used.

### -field lpcStatusText

Type: <b>LPCWSTR</b>

Status text.

### -field dwStatusType

Type: <b>DWORD</b>

One of the values from the <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrstatus">SYNCMGRSTATUS</a> enumeration.

### -field iProgValue

Type: <b>int</b>

An integer that indicates the progress value.

### -field iMaxValue

Type: <b>int</b>

An integer that indicates the maximum progress value.

## -see-also

<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress">ISyncMgrSynchronizeCallback::Progress</a>