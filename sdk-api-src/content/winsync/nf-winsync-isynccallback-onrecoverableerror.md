---
UID: NF:winsync.ISyncCallback.OnRecoverableError
title: ISyncCallback::OnRecoverableError (winsync.h)
description: Occurs when a synchronization provider sets a recoverable error when it is loading or saving an item.
helpviewer_keywords: ["ISyncCallback interface [Windows Sync]","OnRecoverableError method","ISyncCallback.OnRecoverableError","ISyncCallback::OnRecoverableError","OnRecoverableError","OnRecoverableError method [Windows Sync]","OnRecoverableError method [Windows Sync]","ISyncCallback interface","winsync.isynccallback_onrecoverableerror","winsync/ISyncCallback::OnRecoverableError"]
old-location: winsync\isynccallback_onrecoverableerror.htm
tech.root: winsync
ms.assetid: de496e83-cfa4-47c7-9b07-712e59737532
ms.date: 12/05/2018
ms.keywords: ISyncCallback interface [Windows Sync],OnRecoverableError method, ISyncCallback.OnRecoverableError, ISyncCallback::OnRecoverableError, OnRecoverableError, OnRecoverableError method [Windows Sync], OnRecoverableError method [Windows Sync],ISyncCallback interface, winsync.isynccallback_onrecoverableerror, winsync/ISyncCallback::OnRecoverableError
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
 - ISyncCallback::OnRecoverableError
 - winsync/ISyncCallback::OnRecoverableError
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
 - ISyncCallback.OnRecoverableError
---

# ISyncCallback::OnRecoverableError


## -description

Occurs when a synchronization provider sets a recoverable error when it is loading or saving an item.

## -parameters

### -param pRecoverableError [in]

The recoverable error.

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
<dt><b>Application-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback Interface</a>