---
UID: NF:winsync.ISyncSessionState.IsCanceled
title: ISyncSessionState::IsCanceled (winsync.h)
description: Indicates whether the synchronization session has been canceled.
helpviewer_keywords: ["ISyncSessionState interface [Windows Sync]","IsCanceled method","ISyncSessionState.IsCanceled","ISyncSessionState::IsCanceled","IsCanceled","IsCanceled method [Windows Sync]","IsCanceled method [Windows Sync]","ISyncSessionState interface","winsync.isyncsessionstate_iscanceled","winsync/ISyncSessionState::IsCanceled"]
old-location: winsync\isyncsessionstate_iscanceled.htm
tech.root: winsync
ms.assetid: 25ce0e21-99ce-4790-8f53-39466da9226f
ms.date: 12/05/2018
ms.keywords: ISyncSessionState interface [Windows Sync],IsCanceled method, ISyncSessionState.IsCanceled, ISyncSessionState::IsCanceled, IsCanceled, IsCanceled method [Windows Sync], IsCanceled method [Windows Sync],ISyncSessionState interface, winsync.isyncsessionstate_iscanceled, winsync/ISyncSessionState::IsCanceled
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
 - ISyncSessionState::IsCanceled
 - winsync/ISyncSessionState::IsCanceled
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
 - ISyncSessionState.IsCanceled
---

# ISyncSessionState::IsCanceled


## -description

Indicates whether the synchronization session has been canceled.

## -parameters

### -param pfIsCanceled [out]

Returns <b>TRUE</b> if the synchronization session has been canceled; otherwise, returns <b>FALSE</b>.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate">ISyncSessionState Interface</a>