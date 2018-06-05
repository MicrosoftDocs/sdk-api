---
UID: NF:winsync.IEnumRangeExceptions.Clone
title: IEnumRangeExceptions::Clone
author: windows-sdk-content
description: Clones the enumerator and returns a new enumerator that is in the same state as the current one.
old-location: winsync\ienumrangeexceptions_clone.htm
old-project: winsync
ms.assetid: b9ba5d49-754f-4eb0-972b-67e9a6a41994
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: Clone, Clone method [Windows Sync], Clone method [Windows Sync],IEnumRangeExceptions interface, IEnumRangeExceptions interface [Windows Sync],Clone method, IEnumRangeExceptions.Clone, IEnumRangeExceptions::Clone, winsync.ienumrangeexceptions_clone, winsync/IEnumRangeExceptions::Clone
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IEnumRangeExceptions.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IEnumRangeExceptions::Clone


## -description


Clones the enumerator and returns a new enumerator that is in the same state as the current one.


## -parameters




### -param ppEnum [out]

Returns the newly cloned enumerator.


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
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1b2724a3-2f5f-4f30-8cf5-e31f16d4cd14">IEnumRangeExceptions Interface</a>
 

 

