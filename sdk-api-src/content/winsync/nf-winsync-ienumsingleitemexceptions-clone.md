---
UID: NF:winsync.IEnumSingleItemExceptions.Clone
title: IEnumSingleItemExceptions::Clone
author: windows-sdk-content
description: Clones the enumerator and returns a new enumerator that is in the same state as the current one.
old-location: winsync\ienumsingleitemexceptions_clone.htm
old-project: winsync
ms.assetid: 89a02939-e761-450e-9479-29e19a872da6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Clone, Clone method [Windows Sync], Clone method [Windows Sync],IEnumSingleItemExceptions interface, IEnumSingleItemExceptions interface [Windows Sync],Clone method, IEnumSingleItemExceptions.Clone, IEnumSingleItemExceptions::Clone, winsync.ienumsingleitemexceptions_clone, winsync/IEnumSingleItemExceptions::Clone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: winsync.h
req.include-header: 
req.redist: 
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
 - IEnumSingleItemExceptions.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IEnumSingleItemExceptions::Clone


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




<a href="https://msdn.microsoft.com/fed8a258-bc23-454b-9d8a-e3873481b33b">IEnumSingleItemExceptions Interface</a>
 

 

