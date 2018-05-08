---
UID: NF:winsync.ISyncCallback.OnRecoverableError
title: ISyncCallback::OnRecoverableError
author: windows-driver-content
description: Occurs when a synchronization provider sets a recoverable error when it is loading or saving an item.
old-location: winsync\isynccallback_onrecoverableerror.htm
old-project: winsync
ms.assetid: de496e83-cfa4-47c7-9b07-712e59737532
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ISyncCallback interface [Windows Sync],OnRecoverableError method, ISyncCallback.OnRecoverableError, ISyncCallback::OnRecoverableError, OnRecoverableError, OnRecoverableError method [Windows Sync], OnRecoverableError method [Windows Sync],ISyncCallback interface, winsync.isynccallback_onrecoverableerror, winsync/ISyncCallback::OnRecoverableError
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
-	ISyncCallback.OnRecoverableError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncCallback::OnRecoverableError


## -description


Occurs when a synchronization provider sets a recoverable error when it is loading or saving an item.


## -parameters




### -param pRecoverableError [in]

The recoverable error.


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
 




## -see-also




<a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback Interface</a>
 

 

