---
UID: NF:winsync.ISyncSessionState.SetForgottenKnowledgeRecoveryRange
title: ISyncSessionState::SetForgottenKnowledgeRecoveryRange (winsync.h)
author: windows-sdk-content
description: Sets the recovery range when the session is performing forgotten knowledge recovery.
old-location: winsync\isyncsessionstate_setforgottenknowledgerecoveryrange.htm
tech.root: winsync
ms.assetid: 2de6bfb3-bde9-49ee-97eb-acc1671efd0d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncSessionState interface [Windows Sync],SetForgottenKnowledgeRecoveryRange method, ISyncSessionState.SetForgottenKnowledgeRecoveryRange, ISyncSessionState::SetForgottenKnowledgeRecoveryRange, SetForgottenKnowledgeRecoveryRange, SetForgottenKnowledgeRecoveryRange method [Windows Sync], SetForgottenKnowledgeRecoveryRange method [Windows Sync],ISyncSessionState interface, winsync.isyncsessionstate_setforgottenknowledgerecoveryrange, winsync/ISyncSessionState::SetForgottenKnowledgeRecoveryRange
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
 - ISyncSessionState.SetForgottenKnowledgeRecoveryRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncSessionState::SetForgottenKnowledgeRecoveryRange


## -description


Sets the recovery range when the session is performing forgotten knowledge recovery.


## -parameters




### -param pRange [in]

The lower and upper bounds that define the range of IDs to be recovered.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
An item ID in <i>pRange</i> is not in the format that is specified by the ID format schema of the provider.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e">ISyncSessionState Interface</a>
 

 

