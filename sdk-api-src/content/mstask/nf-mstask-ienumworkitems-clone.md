---
UID: NF:mstask.IEnumWorkItems.Clone
title: IEnumWorkItems::Clone (mstask.h)
description: Creates a new enumeration object that contains the same enumeration state as the current enumeration.
helpviewer_keywords: ["Clone","Clone method [Task Scheduler]","Clone method [Task Scheduler]","IEnumWorkItems interface","IEnumWorkItems interface [Task Scheduler]","Clone method","IEnumWorkItems.Clone","IEnumWorkItems::Clone","_msb_ienumworkitems_clone","mstask/IEnumWorkItems::Clone","taskschd.ienumworkitems_clone"]
old-location: taskschd\ienumworkitems_clone.htm
tech.root: taskschd
ms.assetid: c42550df-33ad-49cc-ab89-5f952cce2a83
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Task Scheduler], Clone method [Task Scheduler],IEnumWorkItems interface, IEnumWorkItems interface [Task Scheduler],Clone method, IEnumWorkItems.Clone, IEnumWorkItems::Clone, _msb_ienumworkitems_clone, mstask/IEnumWorkItems::Clone, taskschd.ienumworkitems_clone
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
 - IEnumWorkItems::Clone
 - mstask/IEnumWorkItems::Clone
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
 - IEnumWorkItems.Clone
---

# IEnumWorkItems::Clone


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

  Creates a new enumeration object that contains the same enumeration state as the current enumeration.

Because the new object points to the same place in the enumeration sequence, a client can use the 
<b>Clone</b> method to record a particular point in the enumeration sequence and return to that point later.

## -parameters

### -param ppEnumWorkItems [out]

A pointer to a pointer to a new 
<a href="/windows/desktop/api/mstask/nn-mstask-ienumworkitems">IEnumWorkItems</a> interface. This pointer will point to the newly created enumeration. If the method fails, this parameter is undefined.

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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An error occurred.

</td>
</tr>
</table>

## -remarks

The 
<a href="/windows/desktop/api/mstask/nn-mstask-ienumworkitems">IEnumWorkItems</a> interface also provides methods for retrieving sets of tasks, skipping sets of tasks, and resetting the enumeration sequence.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ienumworkitems">IEnumWorkItems</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ienumworkitems-next">IEnumWorkItems::Next</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ienumworkitems-reset">IEnumWorkItems::Reset</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ienumworkitems-skip">IEnumWorkItems::Skip</a>