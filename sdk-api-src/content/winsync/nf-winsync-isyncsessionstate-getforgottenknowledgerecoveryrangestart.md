---
UID: NF:winsync.ISyncSessionState.GetForgottenKnowledgeRecoveryRangeStart
title: ISyncSessionState::GetForgottenKnowledgeRecoveryRangeStart
author: windows-sdk-content
description: Gets the lower bound of the recovery range when the session is performing forgotten knowledge recovery.
old-location: winsync\isyncsessionstate_getforgottenknowledgerecoveryrangestart.htm
tech.root: winsync
ms.assetid: a6d6434a-d4cf-4b92-958c-5ff8022a9531
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetForgottenKnowledgeRecoveryRangeStart, GetForgottenKnowledgeRecoveryRangeStart method [Windows Sync], GetForgottenKnowledgeRecoveryRangeStart method [Windows Sync],ISyncSessionState interface, ISyncSessionState interface [Windows Sync],GetForgottenKnowledgeRecoveryRangeStart method, ISyncSessionState.GetForgottenKnowledgeRecoveryRangeStart, ISyncSessionState::GetForgottenKnowledgeRecoveryRangeStart, winsync.isyncsessionstate_getforgottenknowledgerecoveryrangestart, winsync/ISyncSessionState::GetForgottenKnowledgeRecoveryRangeStart
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
 - ISyncSessionState.GetForgottenKnowledgeRecoveryRangeStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncSessionState::GetForgottenKnowledgeRecoveryRangeStart


## -description


Gets the lower bound of the recovery range when the session is performing forgotten knowledge recovery.


## -parameters




### -param pbRangeStart [in, out]

Returns the lower bound of the recovery range when the session is performing forgotten knowledge recovery.


### -param pcbRangeStart [in, out]

Specifies the number of bytes in <i>pbRangeStart</i>. Returns the number of bytes required to retrieve the range value when <i>pcbRangeStart</i> is too small, or the number of bytes written.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pcbRangeStart</i> is too small. In this case, the required number of bytes is returned in <i>pcbRangeStart</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e">ISyncSessionState Interface</a>
 

 

