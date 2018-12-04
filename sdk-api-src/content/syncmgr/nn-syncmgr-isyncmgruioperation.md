---
UID: NN:syncmgr.ISyncMgrUIOperation
title: ISyncMgrUIOperation
author: windows-sdk-content
description: Exposes a method through which a sync handler or sync item can display a UI object when requested to do so by Sync Center.
old-location: shell\ISyncMgrUIOperation.htm
tech.root: shell
ms.assetid: 6fa4b0ac-3c75-4cda-b20d-582a3e18fb28
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ISyncMgrUIOperation, ISyncMgrUIOperation interface [Windows Shell], ISyncMgrUIOperation interface [Windows Shell],described, _shell_ISyncMgrUIOperation, shell.ISyncMgrUIOperation, syncmgr/ISyncMgrUIOperation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrUIOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrUIOperation interface


## -description


Exposes a method through which a sync handler or sync item can display a UI object when requested to do so by Sync Center.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrUIOperation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrUIOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrUIOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66dd853e-0fb0-4736-982a-e0183cb51842">Run</a>
</td>
<td align="left" width="63%">
Performs the actual display of UI for a handler or sync item when requested to do so by Sync Center.

</td>
</tr>
</table> 


## -remarks



Handlers implement <b>ISyncMgrUIOperation</b> to provide UI for a particular action. Each separate action (browse, schedule, enable/disable, activate/deactivate, and delete) requires a separate implementation.

A handler should only implement this interface for operations for which it wants to present UI.

The following summarizes the steps Sync Center takes to instantiate and use this interface.
            
                

<ol>
<li>Sync Center creates a separate thread for the UI operation.</li>
<li>Sync Center creates a new instance of the handler.</li>
<li>If the operation involves only a handler, Sync Center calls <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> with the appropriate <b>SYNCMGR_OBJECTID</b> object ID to obtain a pointer to the <b>ISyncMgrUIOperation</b> that implements that UI object. For example, Sync Center calls <b>ISyncMgrHandler::GetObject</b> with <b>SYNCMGR_OBJECTID_QueryBeforeDelete</b> to obtain an object that is called to display UI when the user chooses to delete the handler, asking for a confirmation that they do indeed want to delete it.</li>
<li>If the operation involves a sync item, Sync Center makes a series of calls, including the following: 
                        <ol>
<li>
<a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> is called on the <a href="https://msdn.microsoft.com/39579030-1cf5-4e82-a5e7-cb3415903d02">ISyncMgrHandler</a> interface to retrieve an instance of <a href="https://msdn.microsoft.com/c07487a5-aa12-411d-93bd-3774262e55c6">ISyncMgrSyncItemContainer</a>.</li>
<li>
<a href="https://msdn.microsoft.com/27cdfcfe-d419-4232-b1cc-b9e7b8b2d315">ISyncMgrSyncItemContainer::GetSyncItem</a> is called to obtain a pointer to the <a href="https://msdn.microsoft.com/322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda">ISyncMgrSyncItem</a> instance representing the item.</li>
<li>
<a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">ISyncMgrSyncItem::GetObject</a> is called with the appropriate <b>SYNCMGR_OBJECTID</b> object ID to obtain a pointer to the <b>ISyncMgrUIOperation</b> that implements the UI object.</li>
</ol>
</li>
<li>Sync Center calls the UI object's <a href="https://msdn.microsoft.com/66dd853e-0fb0-4736-982a-e0183cb51842">Run</a> method to display the UI.</li>
</ol>
By implementing the UI as a separate interface, the display of the UI can be performed independently of synchronization. <b>ISyncMgrUIOperation</b> should be implemented on a different object than either <a href="https://msdn.microsoft.com/39579030-1cf5-4e82-a5e7-cb3415903d02">ISyncMgrHandler</a> or <a href="https://msdn.microsoft.com/322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda">ISyncMgrSyncItem</a>.

If the user requests an action, then requests that same action again before the first has completed, the UI for the initial action is activated and brought to the foreground.



