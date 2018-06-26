---
UID: NN:syncmgr.ISyncMgrConflictResolveInfo
title: ISyncMgrConflictResolveInfo
author: windows-sdk-content
description: Exposes methods that get and set information about sync manager conflict resolution.
old-location: shell\ISyncMgrConflictResolveInfo.htm
old-project: shell
ms.assetid: c47d533f-7307-4db3-a025-961f3419203e
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: ISyncMgrConflictResolveInfo, ISyncMgrConflictResolveInfo interface [Windows Shell], ISyncMgrConflictResolveInfo interface [Windows Shell],described, _shell_ISyncMgrConflictResolveInfo, shell.ISyncMgrConflictResolveInfo, syncmgr/ISyncMgrConflictResolveInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflictResolveInfo interface


## -description


Exposes methods that get and set information about sync manager conflict resolution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflictResolveInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrConflictResolveInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3c857e53-756b-44c2-b3fa-6d57c21939e7">GetItemChoice</a>
</td>
<td align="left" width="63%">
Gets the index of an item that the user wants to keep.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7604455c-35ab-4f94-8e5a-3f6aa83fc9cf">GetItemChoiceCount</a>
</td>
<td align="left" width="63%">
Gets the number of items that the user wants to keep.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac22d346-3012-41b0-a655-062f501af621">GetIterationInfo</a>
</td>
<td align="left" width="63%">
Gets information about which conflict in a set of conflicts is being resolved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/277eee0e-3f75-4ed1-8df2-75289838d3e5">GetPresenterChoice</a>
</td>
<td align="left" width="63%">
Gets what kind of choice was made and whether to apply the choice to all subsequent conflicts in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f263f83-1d7c-40c6-a57c-1334a52cd712">GetPresenterNextStep</a>
</td>
<td align="left" width="63%">
Gets what the presenter wants to do as the next step in the sync manager conflict resolution.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4485f49-9bcb-47a8-8559-da2217ee1eab">SetItemChoices</a>
</td>
<td align="left" width="63%">
Sets the array of indexes that represents which items the user wants to keep. This method is used when the user chooses to apply the same operation to all selected conflicts of the same type from the same handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f4bfe69-1ff3-4d21-9c27-f5d8ecfc8371">SetPresenterChoice</a>
</td>
<td align="left" width="63%">
Sets what kind of choice was made about a sync manager conflict resolution and whether to apply the choice to all subsequent conflicts in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a56ca252-89e5-4ad0-bc9a-f8c7b70bd536">SetPresenterNextStep</a>
</td>
<td align="left" width="63%">
Sets what the presenter wants to do as the next step in the sync manager conflict resolution.

</td>
</tr>
</table> 

