---
UID: NS:mobsync._tagSYNCMGRLOGERRORINFO
title: SYNCMGRLOGERRORINFO (mobsync.h)
description: Provides error information for use in the ISyncMgrSynchronizeCallback::LogError method.
helpviewer_keywords: ["*LPSYNCMGRLOGERRORINFO","LPSYNCMGRLOGERRORINFO","LPSYNCMGRLOGERRORINFO structure pointer [Windows Shell]","SYNCMGRERRORFLAG_ENABLEJUMPTEXT","SYNCMGRLOGERRORINFO","SYNCMGRLOGERRORINFO structure [Windows Shell]","SYNCMGRLOGERROR_ERRORFLAGS","SYNCMGRLOGERROR_ERRORID","SYNCMGRLOGERROR_ITEMID","mobsync/LPSYNCMGRLOGERRORINFO","mobsync/SYNCMGRLOGERRORINFO","shell.syncmgr_syncmgrlogerrorinfo","syncmgr.syncmgrlogerrorinfo"]
old-location: shell\syncmgr_syncmgrlogerrorinfo.htm
tech.root: shell
ms.assetid: 0220792c-90e7-4802-9ba3-3fc6ce01e4de
ms.date: 12/05/2018
ms.keywords: '*LPSYNCMGRLOGERRORINFO, LPSYNCMGRLOGERRORINFO, LPSYNCMGRLOGERRORINFO structure pointer [Windows Shell], SYNCMGRERRORFLAG_ENABLEJUMPTEXT, SYNCMGRLOGERRORINFO, SYNCMGRLOGERRORINFO structure [Windows Shell], SYNCMGRLOGERROR_ERRORFLAGS, SYNCMGRLOGERROR_ERRORID, SYNCMGRLOGERROR_ITEMID, mobsync/LPSYNCMGRLOGERRORINFO, mobsync/SYNCMGRLOGERRORINFO, shell.syncmgr_syncmgrlogerrorinfo, syncmgr.syncmgrlogerrorinfo'
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
req.typenames: SYNCMGRLOGERRORINFO, *LPSYNCMGRLOGERRORINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSYNCMGRLOGERRORINFO
 - mobsync/_tagSYNCMGRLOGERRORINFO
 - LPSYNCMGRLOGERRORINFO
 - mobsync/LPSYNCMGRLOGERRORINFO
 - SYNCMGRLOGERRORINFO
 - mobsync/SYNCMGRLOGERRORINFO
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
 - SYNCMGRLOGERRORINFO
---

# SYNCMGRLOGERRORINFO structure


## -description

Provides error information for use in the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror">ISyncMgrSynchronizeCallback::LogError</a> method.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure.

### -field mask

Type: <b>DWORD</b>

The mask value. The synchronization manager handler implemented by your application can set any combination of the following bits to indicate which fields of <b>SYNCMGRLOGERRORINFO</b> it has filled in when calling <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror">ISyncMgrSynchronizeCallback::LogError</a>.



#### SYNCMGRLOGERROR_ERRORFLAGS

The <b>dwSyncMgrErrorFlags</b> field is valid.



#### SYNCMGRLOGERROR_ERRORID

The <b>ErrorID</b> field is valid.



#### SYNCMGRLOGERROR_ITEMID

The <b>ItemID</b> field is valid.

### -field dwSyncMgrErrorFlags

Type: <b>DWORD</b>

Error flags. At this time only the following value is recognized.



#### SYNCMGRERRORFLAG_ENABLEJUMPTEXT

The <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showerror">ISyncMgrSynchronize::ShowError</a> method should be called on this item.

### -field ErrorID

Type: <b>GUID</b>

An error identifier.

### -field ItemID

Type: <b>GUID</b>

The item where the error occurred.

## -see-also

<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror">ISyncMgrSynchronizeCallback::LogError</a>