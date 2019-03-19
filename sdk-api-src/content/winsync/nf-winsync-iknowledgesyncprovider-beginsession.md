---
UID: NF:winsync.IKnowledgeSyncProvider.BeginSession
title: IKnowledgeSyncProvider::BeginSession (winsync.h)
author: windows-sdk-content
description: Notifies the provider that it is joining a synchronization session.
old-location: winsync\iknowledgesyncprovider_beginsession.htm
tech.root: winsync
ms.assetid: 15aae98e-96c6-45f3-906f-1729fa79ebdb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BeginSession, BeginSession method [Windows Sync], BeginSession method [Windows Sync],IKnowledgeSyncProvider interface, IKnowledgeSyncProvider interface [Windows Sync],BeginSession method, IKnowledgeSyncProvider.BeginSession, IKnowledgeSyncProvider::BeginSession, winsync.iknowledgesyncprovider_beginsession, winsync/IKnowledgeSyncProvider::BeginSession
ms.topic: method
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
 - IKnowledgeSyncProvider.BeginSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/396bbf7e-7fd0-4a2e-8304-f87097cd5e50">IKnowledgeSyncProvider Interface</a>
 

 

