---
UID: NF:winsync.IKnowledgeSyncProvider.EndSession
title: IKnowledgeSyncProvider::EndSession method
author: windows-driver-content
description: Notifies the provider that a synchronization session to which it was enlisted has finished.
old-location: winsync\iknowledgesyncprovider_endsession.htm
old-project: winsync
ms.assetid: b726c902-6ccb-4c73-85f1-7256b92ef7e2
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: EndSession method [Windows Sync], EndSession method [Windows Sync], IKnowledgeSyncProvider interface, EndSession,IKnowledgeSyncProvider.EndSession, IKnowledgeSyncProvider, IKnowledgeSyncProvider interface [Windows Sync], EndSession method, IKnowledgeSyncProvider::EndSession, winsync.iknowledgesyncprovider_endsession, winsync/IKnowledgeSyncProvider::EndSession
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IKnowledgeSyncProvider.EndSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IKnowledgeSyncProvider::EndSession method


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



<i>pSessionState</i> will be equal to the <b>ISyncSessionState</b> object that was provided to the previous corresponding call to <a href="https://msdn.microsoft.com/15aae98e-96c6-45f3-906f-1729fa79ebdb">IKnowledgeSyncProvider::BeginSession</a>.

<div class="alert"><b>Note</b>  This method must return an error, typically <a href="https://msdn.microsoft.com/da86cf89-885b-42bc-9fcb-0c9114a36f78">SYNC_E_INVALIDOPERATION</a>, if the provider did not receive a previous call to <a href="https://msdn.microsoft.com/15aae98e-96c6-45f3-906f-1729fa79ebdb">BeginSession</a> for the specified session.

<p class="note">When this method is called, the provider must release any references it has to the <b>ISyncSessionState</b> object that is specified by <i>pSessionState</i>.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/396bbf7e-7fd0-4a2e-8304-f87097cd5e50">IKnowledgeSyncProvider Interface</a>
 

 

