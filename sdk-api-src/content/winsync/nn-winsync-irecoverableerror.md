---
UID: NN:winsync.IRecoverableError
title: IRecoverableError (winsync.h)
description: Represents a recoverable error that occurred when an item was loaded or when an item was saved.
helpviewer_keywords: ["IRecoverableError","IRecoverableError interface [Windows Sync]","IRecoverableError interface [Windows Sync]","described","winsync.irecoverableerror","winsync/IRecoverableError"]
old-location: winsync\irecoverableerror.htm
tech.root: winsync
ms.assetid: a8b8a84a-6083-4696-bef1-46145a4d71c8
ms.date: 12/05/2018
ms.keywords: IRecoverableError, IRecoverableError interface [Windows Sync], IRecoverableError interface [Windows Sync],described, winsync.irecoverableerror, winsync/IRecoverableError
f1_keywords:
- winsync/IRecoverableError
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- winsync.h
api_name:
- IRecoverableError
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRecoverableError interface


## -description


Represents a recoverable error that occurred when an item was loaded or when an item was saved.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRecoverableError</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRecoverableError</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRecoverableError</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-irecoverableerror-getchangewithrecoverableerror">GetChangeWithRecoverableError</a>
</td>
<td align="left" width="63%">
Gets the item change that caused the error.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-irecoverableerror-getprovider">GetProvider</a>
</td>
<td align="left" width="63%">
Gets the role of the provider that skipped the item change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-irecoverableerror-getrecoverableerrordataforchange">GetRecoverableErrorDataForChange</a>
</td>
<td align="left" width="63%">
Gets additional data about the recoverable error.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-irecoverableerror-getrecoverableerrordataforchangeunit">GetRecoverableErrorDataForChangeUnit</a>
</td>
<td align="left" width="63%">
Gets additional data about the recoverable error for a specified change unit.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-irecoverableerror-getstage">GetStage</a>
</td>
<td align="left" width="63%">
Gets the stage in the synchronization session when the error occurred.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

