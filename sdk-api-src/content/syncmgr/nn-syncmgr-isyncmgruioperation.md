---
UID: NN:syncmgr.ISyncMgrUIOperation
title: ISyncMgrUIOperation (syncmgr.h)
description: Exposes a method through which a sync handler or sync item can display a UI object when requested to do so by Sync Center.
helpviewer_keywords: ["ISyncMgrUIOperation","ISyncMgrUIOperation interface [Windows Shell]","ISyncMgrUIOperation interface [Windows Shell]","described","_shell_ISyncMgrUIOperation","shell.ISyncMgrUIOperation","syncmgr/ISyncMgrUIOperation"]
old-location: shell\ISyncMgrUIOperation.htm
tech.root: shell
ms.assetid: 6fa4b0ac-3c75-4cda-b20d-582a3e18fb28
ms.date: 12/05/2018
ms.keywords: ISyncMgrUIOperation, ISyncMgrUIOperation interface [Windows Shell], ISyncMgrUIOperation interface [Windows Shell],described, _shell_ISyncMgrUIOperation, shell.ISyncMgrUIOperation, syncmgr/ISyncMgrUIOperation
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
 - ISyncMgrUIOperation
 - syncmgr/ISyncMgrUIOperation
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
 - ISyncMgrUIOperation
---

# ISyncMgrUIOperation interface


## -description

Exposes a method through which a sync handler or sync item can display a UI object when requested to do so by Sync Center.

## -inheritance

The <b>ISyncMgrUIOperation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrUIOperation</b> also has these types of members:

## -remarks

Handlers implement <b>ISyncMgrUIOperation</b> to provide UI for a particular action. Each separate action (browse, schedule, enable/disable, activate/deactivate, and delete) requires a separate implementation.

A handler should only implement this interface for operations for which it wants to present UI.

The following summarizes the steps Sync Center takes to instantiate and use this interface.
            
                

<ol>
<li>Sync Center creates a separate thread for the UI operation.</li>
<li>Sync Center creates a new instance of the handler.</li>
<li>If the operation involves only a handler, Sync Center calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> with the appropriate <b>SYNCMGR_OBJECTID</b> object ID to obtain a pointer to the <b>ISyncMgrUIOperation</b> that implements that UI object. For example, Sync Center calls <b>ISyncMgrHandler::GetObject</b> with <b>SYNCMGR_OBJECTID_QueryBeforeDelete</b> to obtain an object that is called to display UI when the user chooses to delete the handler, asking for a confirmation that they do indeed want to delete it.</li>
<li>If the operation involves a sync item, Sync Center makes a series of calls, including the following: 
                        <ol>
<li>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> is called on the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a> interface to retrieve an instance of <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer">ISyncMgrSyncItemContainer</a>.</li>
<li>
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem">ISyncMgrSyncItemContainer::GetSyncItem</a> is called to obtain a pointer to the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncitem">ISyncMgrSyncItem</a> instance representing the item.</li>
<li>
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">ISyncMgrSyncItem::GetObject</a> is called with the appropriate <b>SYNCMGR_OBJECTID</b> object ID to obtain a pointer to the <b>ISyncMgrUIOperation</b> that implements the UI object.</li>
</ol>
</li>
<li>Sync Center calls the UI object's <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgruioperation-run">Run</a> method to display the UI.</li>
</ol>
By implementing the UI as a separate interface, the display of the UI can be performed independently of synchronization. <b>ISyncMgrUIOperation</b> should be implemented on a different object than either <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a> or <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncitem">ISyncMgrSyncItem</a>.

If the user requests an action, then requests that same action again before the first has completed, the UI for the initial action is activated and brought to the foreground.
