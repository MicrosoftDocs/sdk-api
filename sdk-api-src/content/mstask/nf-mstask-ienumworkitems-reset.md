---
UID: NF:mstask.IEnumWorkItems.Reset
title: IEnumWorkItems::Reset (mstask.h)
description: Resets the enumeration sequence to the beginning. (IEnumWorkItems.Reset)
helpviewer_keywords: ["IEnumWorkItems interface [Task Scheduler]","Reset method","IEnumWorkItems.Reset","IEnumWorkItems::Reset","Reset","Reset method [Task Scheduler]","Reset method [Task Scheduler]","IEnumWorkItems interface","_msb_ienumworkitems_reset","mstask/IEnumWorkItems::Reset","taskschd.ienumworkitems_reset"]
old-location: taskschd\ienumworkitems_reset.htm
tech.root: taskschd
ms.assetid: 920ba47b-41cd-462b-9b72-73898a5cd4d0
ms.date: 12/05/2018
ms.keywords: IEnumWorkItems interface [Task Scheduler],Reset method, IEnumWorkItems.Reset, IEnumWorkItems::Reset, Reset, Reset method [Task Scheduler], Reset method [Task Scheduler],IEnumWorkItems interface, _msb_ienumworkitems_reset, mstask/IEnumWorkItems::Reset, taskschd.ienumworkitems_reset
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
 - IEnumWorkItems::Reset
 - mstask/IEnumWorkItems::Reset
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
 - IEnumWorkItems.Reset
---

# IEnumWorkItems::Reset


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

 Resets the enumeration sequence to the beginning.



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
The enumeration sequence is reset to the beginning of the list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
</table>

## -remarks

A call to this method does not guarantee that the same set of tasks will be enumerated after the enumeration sequence is reset. Tasks may have been added to or deleted from the collection while you were enumerating the list.

The 
<a href="/windows/desktop/api/mstask/nn-mstask-ienumworkitems">IEnumWorkItems</a> interface also provides methods for retrieving sets of tasks, skipping sets of tasks, and making a copy of the current state of the enumeration.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ienumworkitems">IEnumWorkItems</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ienumworkitems-clone">IEnumWorkItems::Clone</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ienumworkitems-next">IEnumWorkItems::Next</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ienumworkitems-skip">IEnumWorkItems::Skip</a>
