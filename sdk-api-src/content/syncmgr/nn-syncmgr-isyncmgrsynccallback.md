---
UID: NN:syncmgr.ISyncMgrSyncCallback
title: ISyncMgrSyncCallback (syncmgr.h)
description: Exposes methods that allow a synchronization process to report progress and events to Sync Center, or to query whether the process has been canceled.
helpviewer_keywords: ["ISyncMgrSyncCallback","ISyncMgrSyncCallback interface [Windows Shell]","ISyncMgrSyncCallback interface [Windows Shell]","described","_shell_ISyncMgrSyncCallback","shell.ISyncMgrSyncCallback","syncmgr/ISyncMgrSyncCallback"]
old-location: shell\ISyncMgrSyncCallback.htm
tech.root: shell
ms.assetid: 4f2b6dc3-3b81-4c0a-b0a2-b48f13fba397
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncCallback, ISyncMgrSyncCallback interface [Windows Shell], ISyncMgrSyncCallback interface [Windows Shell],described, _shell_ISyncMgrSyncCallback, shell.ISyncMgrSyncCallback, syncmgr/ISyncMgrSyncCallback
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
 - ISyncMgrSyncCallback
 - syncmgr/ISyncMgrSyncCallback
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
 - ISyncMgrSyncCallback
---

# ISyncMgrSyncCallback interface


## -description

Exposes methods that allow a synchronization process to report progress and events to Sync Center, or to query whether the process has been canceled.

## -inheritance

The <b>ISyncMgrSyncCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSyncCallback</b> also has these types of members:

## -remarks

This interface is passed to <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsessioncreator-createsession">ISyncMgrSessionCreator::CreateSession</a>, which in turn is referenced in the call to <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-synchronize">ISyncMgrHandler::Synchronize</a>.

The handler is expected to call this interface to update the folder's progress UI  for each item and to notify Sync Center when it has completed the synchronization of each item.

<b>ISyncMgrSyncCallback</b> is a replacement for <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>.
