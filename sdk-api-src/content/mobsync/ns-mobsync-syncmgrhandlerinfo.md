---
UID: NS:mobsync._tagSYNCMGRHANDLERINFO
title: SYNCMGRHANDLERINFO (mobsync.h)
description: Provides information about the handler for use in the ISyncMgrSynchronize::GetHandlerInfo method.
helpviewer_keywords: ["*LPSYNCMGRHANDLERINFO","LPSYNCMGRHANDLERINFO","LPSYNCMGRHANDLERINFO structure pointer [Windows Shell]","SYNCMGRHANDLERINFO","SYNCMGRHANDLERINFO structure [Windows Shell]","mobsync/LPSYNCMGRHANDLERINFO","mobsync/SYNCMGRHANDLERINFO","shell.syncmgr_syncmgrhandlerinfo","syncmgr.syncmgrhandlerinfo"]
old-location: shell\syncmgr_syncmgrhandlerinfo.htm
tech.root: shell
ms.assetid: 8640796c-e5d0-48c8-b82b-7a153201e7de
ms.date: 12/05/2018
ms.keywords: '*LPSYNCMGRHANDLERINFO, LPSYNCMGRHANDLERINFO, LPSYNCMGRHANDLERINFO structure pointer [Windows Shell], SYNCMGRHANDLERINFO, SYNCMGRHANDLERINFO structure [Windows Shell], mobsync/LPSYNCMGRHANDLERINFO, mobsync/SYNCMGRHANDLERINFO, shell.syncmgr_syncmgrhandlerinfo, syncmgr.syncmgrhandlerinfo'
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
req.typenames: SYNCMGRHANDLERINFO, *LPSYNCMGRHANDLERINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSYNCMGRHANDLERINFO
 - mobsync/_tagSYNCMGRHANDLERINFO
 - LPSYNCMGRHANDLERINFO
 - mobsync/LPSYNCMGRHANDLERINFO
 - SYNCMGRHANDLERINFO
 - mobsync/SYNCMGRHANDLERINFO
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
 - SYNCMGRHANDLERINFO
---

# SYNCMGRHANDLERINFO structure


## -description

Provides information about the handler for use in the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo">ISyncMgrSynchronize::GetHandlerInfo</a> method.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure in bytes.

### -field hIcon

Type: <b>HICON</b>

The icon for the handler.

### -field SyncMgrHandlerFlags

Type: <b>DWORD</b>

The value of the <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrhandlerflags">SYNCMGRHANDLERFLAGS</a> enumeration.

### -field wszHandlerName

Type: <b>WCHAR[MAX_SYNCMGRHANDLERNAME]</b>

The name to use for the handler.

## -see-also

<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo">ISyncMgrSynchronize::GetHandlerInfo</a>



<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrhandlerflags">SYNCMGRHANDLERFLAGS</a>