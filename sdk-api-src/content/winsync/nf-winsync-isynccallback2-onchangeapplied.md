---
UID: NF:winsync.ISyncCallback2.OnChangeApplied
title: ISyncCallback2::OnChangeApplied
author: windows-sdk-content
description: Occurs after a change is successfully applied.
old-location: winsync\isynccallback2_onchangeapplied.htm
old-project: winsync
ms.assetid: 3397ca51-583b-4051-892b-68f505d85ccd
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ISyncCallback2 interface [Windows Sync],OnChangeApplied method, ISyncCallback2.OnChangeApplied, ISyncCallback2::OnChangeApplied, OnChangeApplied, OnChangeApplied method [Windows Sync], OnChangeApplied method [Windows Sync],ISyncCallback2 interface, winsync.isynccallback2_onchangeapplied, winsync/ISyncCallback2::OnChangeApplied
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
 - ISyncCallback2.OnChangeApplied
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncCallback2::OnChangeApplied


## -description


Occurs after a change is successfully applied.


## -parameters




### -param dwChangesApplied [in]

The number of changes that have been successfully applied during the synchronization session. This value is the sum of item changes plus change unit changes.


### -param dwChangesFailed [in]

The number of changes that have failed to apply during the synchronization session. This value is the sum of item changes plus change unit changes.


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
<dt><b>Application-determined error codes</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback Interface</a>



<a href="https://msdn.microsoft.com/d2d690ba-8da2-4d53-a42c-14e4f010bc2d">ISyncCallback2 Interface</a>
 

 

