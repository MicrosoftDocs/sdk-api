---
UID: NF:winsync.IKnowledgeSyncProvider.BeginSession
title: IKnowledgeSyncProvider::BeginSession (winsync.h)
description: Notifies the provider that it is joining a synchronization session.
helpviewer_keywords: ["BeginSession","BeginSession method [Windows Sync]","BeginSession method [Windows Sync]","IKnowledgeSyncProvider interface","IKnowledgeSyncProvider interface [Windows Sync]","BeginSession method","IKnowledgeSyncProvider.BeginSession","IKnowledgeSyncProvider::BeginSession","winsync.iknowledgesyncprovider_beginsession","winsync/IKnowledgeSyncProvider::BeginSession"]
old-location: winsync\iknowledgesyncprovider_beginsession.htm
tech.root: winsync
ms.assetid: 15aae98e-96c6-45f3-906f-1729fa79ebdb
ms.date: 12/05/2018
ms.keywords: BeginSession, BeginSession method [Windows Sync], BeginSession method [Windows Sync],IKnowledgeSyncProvider interface, IKnowledgeSyncProvider interface [Windows Sync],BeginSession method, IKnowledgeSyncProvider.BeginSession, IKnowledgeSyncProvider::BeginSession, winsync.iknowledgesyncprovider_beginsession, winsync/IKnowledgeSyncProvider::BeginSession
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
 - IKnowledgeSyncProvider::BeginSession
 - winsync/IKnowledgeSyncProvider::BeginSession
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
 - IKnowledgeSyncProvider.BeginSession
---

# IKnowledgeSyncProvider::BeginSession


## -description

Notifies the provider that it is joining a synchronization session.

## -parameters

### -param role [in]

The role of this provider, relative to the other provider in the session.

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

The provider must return an error if it cannot begin a session. This can occur when the provider has not been initialized, has an invalid configuration, or is already enlisted in an active session.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iknowledgesyncprovider">IKnowledgeSyncProvider Interface</a>