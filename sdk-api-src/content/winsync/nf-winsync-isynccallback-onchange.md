---
UID: NF:winsync.ISyncCallback.OnChange
title: ISyncCallback::OnChange
author: windows-sdk-content
description: Occurs before a change is applied.
old-location: winsync\isynccallback_onchange.htm
tech.root: winsync
ms.assetid: 16bcc448-8acc-4349-a5d1-0c0764afe2ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncCallback interface [Windows Sync],OnChange method, ISyncCallback.OnChange, ISyncCallback::OnChange, OnChange, OnChange method [Windows Sync], OnChange method [Windows Sync],ISyncCallback interface, winsync.isynccallback_onchange, winsync/ISyncCallback::OnChange
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
 - ISyncCallback.OnChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncCallback::OnChange


## -description


Occurs before a change is applied.


## -parameters




### -param pSyncChange [in]

The item change that is about to be applied.


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
 

 

