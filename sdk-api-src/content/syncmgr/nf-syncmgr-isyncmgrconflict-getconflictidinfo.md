---
UID: NF:syncmgr.ISyncMgrConflict.GetConflictIdInfo
title: ISyncMgrConflict::GetConflictIdInfo (syncmgr.h)
description: Gets information that identifies a conflict within a conflict store.
helpviewer_keywords: ["GetConflictIdInfo","GetConflictIdInfo method [Windows Shell]","GetConflictIdInfo method [Windows Shell]","ISyncMgrConflict interface","ISyncMgrConflict interface [Windows Shell]","GetConflictIdInfo method","ISyncMgrConflict.GetConflictIdInfo","ISyncMgrConflict::GetConflictIdInfo","_shell_ISyncMgrConflict_GetConflictIdInfo","shell.ISyncMgrConflict_GetConflictIdInfo","syncmgr/ISyncMgrConflict::GetConflictIdInfo"]
old-location: shell\ISyncMgrConflict_GetConflictIdInfo.htm
tech.root: shell
ms.assetid: 9686a6e5-5a0a-4520-803e-1660676d9f61
ms.date: 12/05/2018
ms.keywords: GetConflictIdInfo, GetConflictIdInfo method [Windows Shell], GetConflictIdInfo method [Windows Shell],ISyncMgrConflict interface, ISyncMgrConflict interface [Windows Shell],GetConflictIdInfo method, ISyncMgrConflict.GetConflictIdInfo, ISyncMgrConflict::GetConflictIdInfo, _shell_ISyncMgrConflict_GetConflictIdInfo, shell.ISyncMgrConflict_GetConflictIdInfo, syncmgr/ISyncMgrConflict::GetConflictIdInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrConflict::GetConflictIdInfo
 - syncmgr/ISyncMgrConflict::GetConflictIdInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrConflict.GetConflictIdInfo
---

# ISyncMgrConflict::GetConflictIdInfo


## -description

Gets information that identifies a conflict within a conflict store.

## -parameters

### -param pConflictIdInfo [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ns-syncmgr-syncmgr_conflict_id_info">SYNCMGR_CONFLICT_ID_INFO</a>*</b>

A pointer to a conflict ID info structure. See <a href="/windows/desktop/api/syncmgr/ns-syncmgr-syncmgr_conflict_id_info">SYNCMGR_CONFLICT_ID_INFO</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  Each member should be allocated using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. Free each member using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.</div>
<div> </div>
This method contains two opaque blobs: One is the ID uniquely identifying a conflict within a conflict store. The other is optional extra information stored with the conflict that may be used by the implementation when creating conflict objects in <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictstore-bindtoconflict">BindToConflict</a> and <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictstore-removeconflicts">RemoveConflicts</a>.

The size of of the ID blob must be kept short so that the ID may be embedded inside the conflict's pointer to an item identifier list (PIDL) or parsing name.