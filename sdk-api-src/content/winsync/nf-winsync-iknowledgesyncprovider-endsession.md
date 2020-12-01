---
UID: NF:winsync.IKnowledgeSyncProvider.EndSession
title: IKnowledgeSyncProvider::EndSession (winsync.h)
description: Notifies the provider that a synchronization session to which it was enlisted has finished.
helpviewer_keywords: ["EndSession","EndSession method [Windows Sync]","EndSession method [Windows Sync]","IKnowledgeSyncProvider interface","IKnowledgeSyncProvider interface [Windows Sync]","EndSession method","IKnowledgeSyncProvider.EndSession","IKnowledgeSyncProvider::EndSession","winsync.iknowledgesyncprovider_endsession","winsync/IKnowledgeSyncProvider::EndSession"]
old-location: winsync\iknowledgesyncprovider_endsession.htm
tech.root: winsync
ms.assetid: b726c902-6ccb-4c73-85f1-7256b92ef7e2
ms.date: 12/05/2018
ms.keywords: EndSession, EndSession method [Windows Sync], EndSession method [Windows Sync],IKnowledgeSyncProvider interface, IKnowledgeSyncProvider interface [Windows Sync],EndSession method, IKnowledgeSyncProvider.EndSession, IKnowledgeSyncProvider::EndSession, winsync.iknowledgesyncprovider_endsession, winsync/IKnowledgeSyncProvider::EndSession
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
 - IKnowledgeSyncProvider::EndSession
 - winsync/IKnowledgeSyncProvider::EndSession
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
 - IKnowledgeSyncProvider.EndSession
---

# IKnowledgeSyncProvider::EndSession


## -description

Notifies the provider that a synchronization session to which it was enlisted has finished.

## -parameters

### -param pSessionState [in]

The current status of the corresponding session.

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
<dt><b>Provider-determined error codes</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

<i>pSessionState</i> will be equal to the <b>ISyncSessionState</b> object that was provided to the previous corresponding call to <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-beginsession">IKnowledgeSyncProvider::BeginSession</a>.

<div class="alert"><b>Note</b>  This method must return an error, typically <a href="/previous-versions/windows/desktop/winsync/windows-sync-error-codes">SYNC_E_INVALIDOPERATION</a>, if the provider did not receive a previous call to <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iknowledgesyncprovider-beginsession">BeginSession</a> for the specified session.

<p class="note">When this method is called, the provider must release any references it has to the <b>ISyncSessionState</b> object that is specified by <i>pSessionState</i>.

</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iknowledgesyncprovider">IKnowledgeSyncProvider Interface</a>