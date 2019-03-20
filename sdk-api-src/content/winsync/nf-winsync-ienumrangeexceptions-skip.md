---
UID: NF:winsync.IEnumRangeExceptions.Skip
title: IEnumRangeExceptions::Skip (winsync.h)
author: windows-sdk-content
description: Skips the specified number of range exceptions.
old-location: winsync\ienumrangeexceptions_skip.htm
tech.root: winsync
ms.assetid: 61907858-4089-4c12-865c-623a43132be3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumRangeExceptions interface [Windows Sync],Skip method, IEnumRangeExceptions.Skip, IEnumRangeExceptions::Skip, Skip, Skip method [Windows Sync], Skip method [Windows Sync],IEnumRangeExceptions interface, winsync.ienumrangeexceptions_skip, winsync/IEnumRangeExceptions::Skip
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
 - IEnumRangeExceptions.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumRangeExceptions::Skip


## -description


Skips the specified number of range exceptions.


## -parameters




### -param cExceptions [in]

The number of range exceptions to skip.


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
The enumerator reaches the end of the list before it can skip <i>cExceptions</i> range exceptions. In this case, the enumerator skips as many elements as possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARGS</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1b2724a3-2f5f-4f30-8cf5-e31f16d4cd14">IEnumRangeExceptions Interface</a>
 

 

