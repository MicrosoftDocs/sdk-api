---
UID: NF:winsync.ISyncSessionState.OnProgress
title: ISyncSessionState::OnProgress
author: windows-sdk-content
description: Reports synchronization progress to the application.
old-location: winsync\isyncsessionstate_onprogress.htm
tech.root: winsync
ms.assetid: a2983f9c-ed2d-47b4-bec7-b00dc4d75f3f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISyncSessionState interface [Windows Sync],OnProgress method, ISyncSessionState.OnProgress, ISyncSessionState::OnProgress, OnProgress, OnProgress method [Windows Sync], OnProgress method [Windows Sync],ISyncSessionState interface, winsync.isyncsessionstate_onprogress, winsync/ISyncSessionState::OnProgress
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
 - ISyncSessionState.OnProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncSessionState::OnProgress


## -description


Reports synchronization progress to the application.


## -parameters




### -param provider [in]

The role of the provider that is sending this event.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>provider</i> or <i>syncStage</i> is not a valid value.

</td>
</tr>
</table>
 




## -remarks



This method can be used to report custom progress to the application. When a provider calls this method, the <a href="https://msdn.microsoft.com/4a4dad07-b169-4767-a118-3b5c6c8b9764">ISyncCallback::OnProgress</a> event is raised.




## -see-also




<a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback Interface</a>



<a href="https://msdn.microsoft.com/9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e">ISyncSessionState Interface</a>



<a href="https://msdn.microsoft.com/06f8542a-d742-4cbb-bb44-c107b59ad38f">SYNC_PROGRESS STAGE Enumeration</a>



<a href="https://msdn.microsoft.com/2409c8bf-c4fc-4986-8dde-cc11f0d52ed4">SYNC_PROVIDER ROLE Enumeration</a>
 

 

