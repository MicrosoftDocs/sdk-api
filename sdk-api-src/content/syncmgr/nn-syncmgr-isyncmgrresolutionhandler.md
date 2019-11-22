---
UID: NN:syncmgr.ISyncMgrResolutionHandler
title: ISyncMgrResolutionHandler (syncmgr.h)

description: Exposes methods that manage synchronizing conflicts. Implement this interface to construct a sync conflict handler. The conflict resolution user interface (UI) will call this interface to resolve the conflict presented to the user.
old-location: shell\ISyncMgrResolutionHandler.htm
tech.root: shell
ms.assetid: 5b77217d-5c63-41be-b4df-338714a90fb9

ms.date: 12/05/2018
ms.keywords: ISyncMgrResolutionHandler, ISyncMgrResolutionHandler interface [Windows Shell], ISyncMgrResolutionHandler interface [Windows Shell],described, _shell_ISyncMgrResolutionHandler, shell.ISyncMgrResolutionHandler, syncmgr/ISyncMgrResolutionHandler
ms.topic: interface
f1_keywords: 
 - "syncmgr/ISyncMgrResolutionHandler"
dev_langs:
 - c++
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
 - ISyncMgrResolutionHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrResolutionHandler interface


## -description


Exposes methods that manage synchronizing conflicts. Implement this interface to construct a sync conflict handler. The conflict resolution user interface (UI) will call this interface to resolve the conflict presented to the user.
       


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrResolutionHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrResolutionHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrResolutionHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-keepitems">KeepItems</a>
</td>
<td align="left" width="63%">
Keeps the Shell items that are passed in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-keepother">KeepOther</a>
</td>
<td align="left" width="63%">
Replaces the versions in conflict with a different Shell item that is usually a merged version of the originals.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-keeprecent">KeepRecent</a>
</td>
<td align="left" width="63%">
Keeps the more recent copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-queryabilities">QueryAbilities</a>
</td>
<td align="left" width="63%">
Determines what options the conflict presenter will display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-removefromsyncset">RemoveFromSyncSet</a>
</td>
<td align="left" width="63%">
Deletes the conflict and removes the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>  from synchronization.

</td>
</tr>
</table> 

