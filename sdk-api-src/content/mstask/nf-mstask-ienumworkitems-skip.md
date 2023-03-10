---
UID: NF:mstask.IEnumWorkItems.Skip
title: IEnumWorkItems::Skip (mstask.h)
description: Skips the next specified number of tasks in the enumeration sequence.
helpviewer_keywords: ["IEnumWorkItems interface [Task Scheduler]","Skip method","IEnumWorkItems.Skip","IEnumWorkItems::Skip","Skip","Skip method [Task Scheduler]","Skip method [Task Scheduler]","IEnumWorkItems interface","_msb_ienumworkitems_skip","mstask/IEnumWorkItems::Skip","taskschd.ienumworkitems_skip"]
old-location: taskschd\ienumworkitems_skip.htm
tech.root: taskschd
ms.assetid: 5f4c7c98-a802-4fc3-b88f-bb37826f8199
ms.date: 12/05/2018
ms.keywords: IEnumWorkItems interface [Task Scheduler],Skip method, IEnumWorkItems.Skip, IEnumWorkItems::Skip, Skip, Skip method [Task Scheduler], Skip method [Task Scheduler],IEnumWorkItems interface, _msb_ienumworkitems_skip, mstask/IEnumWorkItems::Skip, taskschd.ienumworkitems_skip
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - IEnumWorkItems::Skip
 - mstask/IEnumWorkItems::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IEnumWorkItems.Skip
---

# IEnumWorkItems::Skip


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Skips the next specified number of tasks in the enumeration sequence.

## -parameters

### -param celt [in]

The number of tasks to be skipped.

## -returns

Returns one of the following values.

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
The number of elements skipped equals <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of elements remaining in the sequence is less than the value specified in <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>celt</i> is less than or equal to zero.

</td>
</tr>
</table>

## -remarks

The 
<a href="/windows/desktop/api/mstask/nn-mstask-ienumworkitems">IEnumWorkItems</a> interface also provides methods for retrieving sets of tasks, resetting the enumeration sequence, and making a copy of the current state of the enumeration.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ienumworkitems">IEnumWorkItems</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ienumworkitems-clone">IEnumWorkItems::Clone</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ienumworkitems-next">IEnumWorkItems::Next</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ienumworkitems-reset">IEnumWorkItems::Reset</a>