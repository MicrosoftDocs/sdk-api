---
UID: NN:syncmgr.ISyncMgrConflictStore
title: ISyncMgrConflictStore (syncmgr.h)
description: Exposes methods that allow a handler to provide conflicts that appear in the Conflicts folder.
helpviewer_keywords: ["ISyncMgrConflictStore","ISyncMgrConflictStore interface [Windows Shell]","ISyncMgrConflictStore interface [Windows Shell]","described","_shell_ISyncMgrConflictStore","shell.ISyncMgrConflictStore","syncmgr/ISyncMgrConflictStore"]
old-location: shell\ISyncMgrConflictStore.htm
tech.root: shell
ms.assetid: 25f47c73-eb9f-4beb-aa10-4f12b38d6507
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictStore, ISyncMgrConflictStore interface [Windows Shell], ISyncMgrConflictStore interface [Windows Shell],described, _shell_ISyncMgrConflictStore, shell.ISyncMgrConflictStore, syncmgr/ISyncMgrConflictStore
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
 - ISyncMgrConflictStore
 - syncmgr/ISyncMgrConflictStore
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
 - ISyncMgrConflictStore
---

# ISyncMgrConflictStore interface


## -description

Exposes methods that allow a handler to provide conflicts that appear in the Conflicts folder.

## -inheritance

The <b>ISyncMgrConflictStore</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrConflictStore</b> also has these types of members:

## -remarks

Conflict is provided to enable the user to select a version of a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> as needed, instead of being forced to pick to complete a sync selection set. The fact that we current display them in the conflict folder is purely secondary. 

The conflict store must notify sync center when its contents change. Nothing is assumed to happen to conflicts when methods are called that affect the conflict. This includes when they are resolved.

Sync Center requests a conflict store from a handler by calling <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> with SYNCMGR_OBJECTID_ConflictStore if the mask returned from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">ISyncMgrHandler::GetCapabilities</a> includes SYNCMGR_HCM_CONFLICT_STORE. The handler can also provide an event store filtered by item by setting the SYNCMGR_ICM_CONFLICT_STORE flag in the mask returned from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">ISyncMgrSyncItem::GetCapabilities</a>.

If conflicts are added to the conflict store, the handler (or a related component) should call <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateconflicts">ISyncMgrControl::UpdateConflicts</a> so that both the Conflicts folder and conflict counts can be updated.
