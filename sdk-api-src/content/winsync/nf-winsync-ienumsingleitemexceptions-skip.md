---
UID: NF:winsync.IEnumSingleItemExceptions.Skip
title: IEnumSingleItemExceptions::Skip
author: windows-sdk-content
description: Skips the specified number of single-item exceptions.
old-location: winsync\ienumsingleitemexceptions_skip.htm
old-project: winsync
ms.assetid: 80e3bb55-b467-4fa4-bb3e-70233e5b0265
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IEnumSingleItemExceptions interface [Windows Sync],Skip method, IEnumSingleItemExceptions.Skip, IEnumSingleItemExceptions::Skip, Skip, Skip method [Windows Sync], Skip method [Windows Sync],IEnumSingleItemExceptions interface, winsync.ienumsingleitemexceptions_skip, winsync/IEnumSingleItemExceptions::Skip
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
 - IEnumSingleItemExceptions.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IEnumSingleItemExceptions::Skip


## -description


Skips the specified number of single-item exceptions.


## -parameters




### -param cExceptions [in]

The number of single-item exceptions to skip.


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
<td width="60%">
The enumerator reaches the end of the list before it can skip <i>cExceptions</i> single-item exceptions. In this case, the enumerator skips as many elements as possible.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fed8a258-bc23-454b-9d8a-e3873481b33b">IEnumSingleItemExceptions Interface</a>
 

 

