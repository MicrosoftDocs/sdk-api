---
UID: NN:syncmgr.ISyncMgrConflictResolveInfo
title: ISyncMgrConflictResolveInfo (syncmgr.h)
author: windows-sdk-content
description: Exposes methods that get and set information about sync manager conflict resolution.
old-location: shell\ISyncMgrConflictResolveInfo.htm
tech.root: shell
ms.assetid: c47d533f-7307-4db3-a025-961f3419203e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictResolveInfo, ISyncMgrConflictResolveInfo interface [Windows Shell], ISyncMgrConflictResolveInfo interface [Windows Shell],described, _shell_ISyncMgrConflictResolveInfo, shell.ISyncMgrConflictResolveInfo, syncmgr/ISyncMgrConflictResolveInfo
ms.topic: interface
f1_keywords: ["syncmgr/ISyncMgrConflictResolveInfo"]
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
 - ISyncMgrConflictResolveInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrConflictResolveInfo interface


## -description


Exposes methods that get and set information about sync manager conflict resolution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflictResolveInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrConflictResolveInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrConflictResolveInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getitemchoice">GetItemChoice</a>
</td>
<td align="left" width="63%">
Gets the index of an item that the user wants to keep.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getitemchoicecount">GetItemChoiceCount</a>
</td>
<td align="left" width="63%">
Gets the number of items that the user wants to keep.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getiterationinfo">GetIterationInfo</a>
</td>
<td align="left" width="63%">
Gets information about which conflict in a set of conflicts is being resolved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getpresenterchoice">GetPresenterChoice</a>
</td>
<td align="left" width="63%">
Gets what kind of choice was made and whether to apply the choice to all subsequent conflicts in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-getpresenternextstep">GetPresenterNextStep</a>
</td>
<td align="left" width="63%">
Gets what the presenter wants to do as the next step in the sync manager conflict resolution.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-setitemchoices">SetItemChoices</a>
</td>
<td align="left" width="63%">
Sets the array of indexes that represents which items the user wants to keep. This method is used when the user chooses to apply the same operation to all selected conflicts of the same type from the same handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-setpresenterchoice">SetPresenterChoice</a>
</td>
<td align="left" width="63%">
Sets what kind of choice was made about a sync manager conflict resolution and whether to apply the choice to all subsequent conflicts in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictresolveinfo-setpresenternextstep">SetPresenterNextStep</a>
</td>
<td align="left" width="63%">
Sets what the presenter wants to do as the next step in the sync manager conflict resolution.

</td>
</tr>
</table> 

