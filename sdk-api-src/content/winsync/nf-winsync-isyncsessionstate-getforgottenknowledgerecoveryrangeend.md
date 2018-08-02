---
UID: NF:winsync.ISyncSessionState.GetForgottenKnowledgeRecoveryRangeEnd
title: ISyncSessionState::GetForgottenKnowledgeRecoveryRangeEnd
author: windows-sdk-content
description: Gets the upper bound of the recovery range when the session is performing forgotten knowledge recovery.
old-location: winsync\isyncsessionstate_getforgottenknowledgerecoveryrangeend.htm
old-project: winsync
ms.assetid: 9ba23805-cb1a-4178-a230-8091e3938fb6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetForgottenKnowledgeRecoveryRangeEnd, GetForgottenKnowledgeRecoveryRangeEnd method [Windows Sync], GetForgottenKnowledgeRecoveryRangeEnd method [Windows Sync],ISyncSessionState interface, ISyncSessionState interface [Windows Sync],GetForgottenKnowledgeRecoveryRangeEnd method, ISyncSessionState.GetForgottenKnowledgeRecoveryRangeEnd, ISyncSessionState::GetForgottenKnowledgeRecoveryRangeEnd, winsync.isyncsessionstate_getforgottenknowledgerecoveryrangeend, winsync/ISyncSessionState::GetForgottenKnowledgeRecoveryRangeEnd
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncSessionState.GetForgottenKnowledgeRecoveryRangeEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncSessionState::GetForgottenKnowledgeRecoveryRangeEnd


## -description


Gets the upper bound of the recovery range when the session is performing forgotten knowledge recovery.


## -parameters




### -param pbRangeEnd [in, out]

Returns the upper bound of the recovery range when the session is performing forgotten knowledge recovery.


### -param pcbRangeEnd [in, out]

Specifies the number of bytes in <i>pbRangeEnd</i>. Returns the number of bytes required to retrieve the range value when <i>pcbRangeEnd</i> is too small, or the number of bytes written.


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
<i>pcbRangeEnd</i> is too small. In this case, the required number of bytes is returned in <i>pcbRangeEnd</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e">ISyncSessionState Interface</a>
 

 

