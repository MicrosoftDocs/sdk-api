---
UID: NN:syncmgr.ISyncMgrConflictFolder
title: ISyncMgrConflictFolder (syncmgr.h)
author: windows-sdk-content
description: Exposes a method that gets the conflict ID list for a conflict object.
old-location: shell\ISyncMgrConflictFolder.htm
tech.root: shell
ms.assetid: de4bb2b2-ebb2-4ab8-afba-3f00a69d51a8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncMgrConflictFolder, ISyncMgrConflictFolder interface [Windows Shell], ISyncMgrConflictFolder interface [Windows Shell],described, _shell_ISyncMgrConflictFolder, shell.ISyncMgrConflictFolder, syncmgr/ISyncMgrConflictFolder
ms.topic: interface
f1_keywords: 
 - "syncmgr/ISyncMgrConflictFolder"
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
 - ISyncMgrConflictFolder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrConflictFolder interface


## -description


Exposes a method that gets the conflict ID list for a conflict object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflictFolder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrConflictFolder</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictfolder-getconflictidlist">GetConflictIDList</a>
</td>
<td align="left" width="63%">
Maps a conflict to its <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

</td>
</tr>
</table> 

