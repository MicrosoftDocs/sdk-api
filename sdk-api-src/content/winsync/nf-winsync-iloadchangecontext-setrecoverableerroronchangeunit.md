---
UID: NF:winsync.ILoadChangeContext.SetRecoverableErrorOnChangeUnit
title: ILoadChangeContext::SetRecoverableErrorOnChangeUnit (winsync.h)
description: Indicates that a recoverable error occurred when data for the specified change unit was loaded from the item store.
helpviewer_keywords: ["ILoadChangeContext interface [Windows Sync]","SetRecoverableErrorOnChangeUnit method","ILoadChangeContext.SetRecoverableErrorOnChangeUnit","ILoadChangeContext::SetRecoverableErrorOnChangeUnit","SetRecoverableErrorOnChangeUnit","SetRecoverableErrorOnChangeUnit method [Windows Sync]","SetRecoverableErrorOnChangeUnit method [Windows Sync]","ILoadChangeContext interface","winsync.iloadchangecontext_setrecoverableerroronchangeunit","winsync/ILoadChangeContext::SetRecoverableErrorOnChangeUnit"]
old-location: winsync\iloadchangecontext_setrecoverableerroronchangeunit.htm
tech.root: winsync
ms.assetid: 0489a26c-5760-4e41-84c9-45868d27b67c
ms.date: 12/05/2018
ms.keywords: ILoadChangeContext interface [Windows Sync],SetRecoverableErrorOnChangeUnit method, ILoadChangeContext.SetRecoverableErrorOnChangeUnit, ILoadChangeContext::SetRecoverableErrorOnChangeUnit, SetRecoverableErrorOnChangeUnit, SetRecoverableErrorOnChangeUnit method [Windows Sync], SetRecoverableErrorOnChangeUnit method [Windows Sync],ILoadChangeContext interface, winsync.iloadchangecontext_setrecoverableerroronchangeunit, winsync/ILoadChangeContext::SetRecoverableErrorOnChangeUnit
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILoadChangeContext::SetRecoverableErrorOnChangeUnit
 - winsync/ILoadChangeContext::SetRecoverableErrorOnChangeUnit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ILoadChangeContext.SetRecoverableErrorOnChangeUnit
---

# ILoadChangeContext::SetRecoverableErrorOnChangeUnit


## -description

Indicates that a recoverable error occurred when data for the specified change unit was loaded from the item store.

## -parameters

### -param hrError [in]

The error code that is associated with the error that prevented the change unit data from being loaded.

### -param pChangeUnit [in]

The change unit change that caused the error.

### -param pErrorData [in]

Additional information about the error.

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
<td width="60%">
<i>hrError</i> does not specify an error.

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
<dt><b>SYNC_E_ON_CREATE_MUST_FAIL_ENTIRE_ITEM</b></dt>
</dl>
</td>
<td width="60%">
The change that contains this change unit refers to an item creation. In this case, the error must be reported on the item change by using <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iloadchangecontext-setrecoverableerroronchange">ILoadChangeContext::SetRecoverableErrorOnChange</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
 An internal error has occurred.

</td>
</tr>
</table>

## -remarks

When this method is called, an <b>IChangeUnitException</b> object is added to the learned knowledge; and the change unit change will not be enumerated again for the duration of the synchronization session.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitexception">IChangeUnitException Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iloadchangecontext">ILoadChangeContext Interface</a>