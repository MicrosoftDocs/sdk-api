---
UID: NN:winsync.ILoadChangeContext
title: ILoadChangeContext (winsync.h)
description: Represents information about a change to be loaded from the item store.
helpviewer_keywords: ["ILoadChangeContext","ILoadChangeContext interface [Windows Sync]","ILoadChangeContext interface [Windows Sync]","described","winsync.iloadchangecontext","winsync/ILoadChangeContext"]
old-location: winsync\iloadchangecontext.htm
tech.root: winsync
ms.assetid: 11d8971b-354f-4347-9d3f-6d32df8dc9d2
ms.date: 12/05/2018
ms.keywords: ILoadChangeContext, ILoadChangeContext interface [Windows Sync], ILoadChangeContext interface [Windows Sync],described, winsync.iloadchangecontext, winsync/ILoadChangeContext
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ILoadChangeContext
 - winsync/ILoadChangeContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ILoadChangeContext
---

# ILoadChangeContext interface


## -description

Represents information about a change to be loaded from the item store.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILoadChangeContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILoadChangeContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILoadChangeContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iloadchangecontext-getsyncchange">GetSyncChange</a>
</td>
<td align="left" width="63%">
Gets the change item for which the change data should be retrieved from the item store.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iloadchangecontext-setrecoverableerroronchange">SetRecoverableErrorOnChange</a>
</td>
<td align="left" width="63%">
Indicates that a recoverable error occurred when data for this item was loaded from the item store.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iloadchangecontext-setrecoverableerroronchangeunit">SetRecoverableErrorOnChangeUnit</a>
</td>
<td align="left" width="63%">
Indicates that a recoverable error occurred when data for the specified change unit was loaded from the item store.


</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>