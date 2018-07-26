---
UID: NN:syncmgr.ISyncMgrConflictFolder
title: ISyncMgrConflictFolder
author: windows-sdk-content
description: Exposes a method that gets the conflict ID list for a conflict object.
old-location: shell\ISyncMgrConflictFolder.htm
old-project: shell
ms.assetid: de4bb2b2-ebb2-4ab8-afba-3f00a69d51a8
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: ISyncMgrConflictFolder, ISyncMgrConflictFolder interface [Windows Shell], ISyncMgrConflictFolder interface [Windows Shell],described, _shell_ISyncMgrConflictFolder, shell.ISyncMgrConflictFolder, syncmgr/ISyncMgrConflictFolder
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
 - ISyncMgrConflictFolder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflictFolder interface


## -description


Exposes a method that gets the conflict ID list for a conflict object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflictFolder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrConflictFolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrConflictFolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a0794dd-ffa6-4a7b-af1a-1605092ead07">GetConflictIDList</a>
</td>
<td align="left" width="63%">
Maps a conflict to its <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.

</td>
</tr>
</table> 

