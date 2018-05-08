---
UID: NF:winsync.ILoadChangeContext.GetSyncChange
title: ILoadChangeContext::GetSyncChange
author: windows-driver-content
description: Gets the change item for which the change data should be retrieved from the item store.
old-location: winsync\iloadchangecontext_getsyncchange.htm
old-project: winsync
ms.assetid: 6ac425bc-f6ec-4a95-b351-01f9eb27a744
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetSyncChange, GetSyncChange method [Windows Sync], GetSyncChange method [Windows Sync],ILoadChangeContext interface, ILoadChangeContext interface [Windows Sync],GetSyncChange method, ILoadChangeContext.GetSyncChange, ILoadChangeContext::GetSyncChange, winsync.iloadchangecontext_getsyncchange, winsync/ILoadChangeContext::GetSyncChange
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
-	ILoadChangeContext.GetSyncChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ILoadChangeContext::GetSyncChange


## -description


Gets the change item for which the change data should be retrieved from the item store.


## -parameters




### -param ppSyncChange [out]

Returns the change item for which the change data should be retrieved from the item store.


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
<dt><b>SYNC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
 When an internal error occurs.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/11d8971b-354f-4347-9d3f-6d32df8dc9d2">ILoadChangeContext Interface</a>



<a href="https://msdn.microsoft.com/d59a5198-5878-4a48-b6c4-042afc36054d">ISynchronousDataRetriever Interface</a>
 

 

