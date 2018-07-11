---
UID: NF:winsync.IEnumSyncChanges.Next
title: IEnumSyncChanges::Next
author: windows-sdk-content
description: Returns the next item change.
old-location: winsync\ienumsyncchanges_next.htm
old-project: winsync
ms.assetid: 23b5f46f-87f3-431e-a253-d349eed27082
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IEnumSyncChanges interface [Windows Sync],Next method, IEnumSyncChanges.Next, IEnumSyncChanges::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumSyncChanges interface, winsync.ienumsyncchanges_next, winsync/IEnumSyncChanges::Next
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
 - IEnumSyncChanges.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IEnumSyncChanges::Next


## -description


Returns the next item change.


## -parameters




### -param cChanges [in]

The number of changes to fetch. The only valid value is 1.


### -param ppChange [out]

Returns the next item change.


### -param pcFetched [in, out]

Returns the number of changes that are fetched.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c3f27c6d-4fc1-420c-afc1-0bd2bdbd6ab2">IEnumSyncChanges Interface</a>
 

 

