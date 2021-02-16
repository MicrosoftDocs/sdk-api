---
UID: NF:winsync.ISyncCallback.OnProgress
title: ISyncCallback::OnProgress (winsync.h)
description: Occurs periodically during the synchronization session to report progress.
helpviewer_keywords: ["ISyncCallback interface [Windows Sync]","OnProgress method","ISyncCallback.OnProgress","ISyncCallback::OnProgress","OnProgress","OnProgress method [Windows Sync]","OnProgress method [Windows Sync]","ISyncCallback interface","winsync.isynccallback_onprogress","winsync/ISyncCallback::OnProgress"]
old-location: winsync\isynccallback_onprogress.htm
tech.root: winsync
ms.assetid: 4a4dad07-b169-4767-a118-3b5c6c8b9764
ms.date: 12/05/2018
ms.keywords: ISyncCallback interface [Windows Sync],OnProgress method, ISyncCallback.OnProgress, ISyncCallback::OnProgress, OnProgress, OnProgress method [Windows Sync], OnProgress method [Windows Sync],ISyncCallback interface, winsync.isynccallback_onprogress, winsync/ISyncCallback::OnProgress
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
 - ISyncCallback::OnProgress
 - winsync/ISyncCallback::OnProgress
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
 - ISyncCallback.OnProgress
---

# ISyncCallback::OnProgress


## -description

Occurs periodically during the synchronization session to report progress.

## -parameters

### -param provider [in]

The role of the provider that is associated with this event.

### -param syncStage [in]

The current stage of the synchronization session.

### -param dwCompletedWork [in]

The amount of work that is currently completed in the session. This value is interpreted as being a part of <i>dwTotalWork</i>.

### -param dwTotalWork [in]

The total work for the session.

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

## -remarks

Exactly when <b>OnProgress</b> is sent and with what values depends on the providers.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback Interface</a>