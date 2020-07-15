---
UID: NN:shobjidl_core.IFileSyncMergeHandler
title: IFileSyncMergeHandler (shobjidl_core.h)
description: .
helpviewer_keywords: ["IFileSyncMergeHandler","IFileSyncMergeHandler interface [Windows Shell]","IFileSyncMergeHandler interface [Windows Shell]","described","shell.IFileSyncMergeHandler","shobjidl_core/IFileSyncMergeHandler"]
old-location: shell\IFileSyncMergeHandler.htm
tech.root: shell
ms.assetid: 467BF7B9-184E-409F-B5B7-F95E9891C2CD
ms.date: 12/05/2018
ms.keywords: IFileSyncMergeHandler, IFileSyncMergeHandler interface [Windows Shell], IFileSyncMergeHandler interface [Windows Shell],described, shell.IFileSyncMergeHandler, shobjidl_core/IFileSyncMergeHandler
f1_keywords:
- shobjidl_core/IFileSyncMergeHandler
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
- shobjidl_core.h
api_name:
- IFileSyncMergeHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileSyncMergeHandler interface


## -description

Exposed methods to handle file sync operations between a local copy and a server copy of a file.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSyncMergeHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileSyncMergeHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSyncMergeHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesyncmergehandler-merge">Merge</a>
</td>
<td align="left" width="63%">Merges changes between the local copy and server copy of a file.</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesyncmergehandler-showresolveconflictuiasync">ShowResolveConflictUIAsync</a>
</td>
<td align="left" width="63%">Displays a UI to resolve conflicts between the local copy and server copy of a file.</td>
</tr>
</table> 

