---
UID: NF:reconcil.IReconcilableObject.GetProgressFeedbackMaxEstimate
title: IReconcilableObject::GetProgressFeedbackMaxEstimate (reconcil.h)
description: Retrieves an estimated measurement of the amount of work required to complete a reconciliation.
helpviewer_keywords: ["GetProgressFeedbackMaxEstimate","GetProgressFeedbackMaxEstimate method [Legacy Windows Environment Features]","GetProgressFeedbackMaxEstimate method [Legacy Windows Environment Features]","IReconcilableObject interface","IReconcilableObject interface [Legacy Windows Environment Features]","GetProgressFeedbackMaxEstimate method","IReconcilableObject.GetProgressFeedbackMaxEstimate","IReconcilableObject::GetProgressFeedbackMaxEstimate","_win32_IReconcilableObject_GetProgressFeedbackMaxEstimate","lwef.ireconcilableobject_getprogressfeedbackmaxestimate","reconcil/IReconcilableObject::GetProgressFeedbackMaxEstimate","shell.ireconcilableobject_getprogressfeedbackmaxestimate"]
old-location: lwef\ireconcilableobject_getprogressfeedbackmaxestimate.htm
tech.root: lwef
ms.assetid: fdaa7f59-3aba-4a9e-b394-a76029ddab13
ms.date: 12/05/2018
ms.keywords: GetProgressFeedbackMaxEstimate, GetProgressFeedbackMaxEstimate method [Legacy Windows Environment Features], GetProgressFeedbackMaxEstimate method [Legacy Windows Environment Features],IReconcilableObject interface, IReconcilableObject interface [Legacy Windows Environment Features],GetProgressFeedbackMaxEstimate method, IReconcilableObject.GetProgressFeedbackMaxEstimate, IReconcilableObject::GetProgressFeedbackMaxEstimate, _win32_IReconcilableObject_GetProgressFeedbackMaxEstimate, lwef.ireconcilableobject_getprogressfeedbackmaxestimate, reconcil/IReconcilableObject::GetProgressFeedbackMaxEstimate, shell.ireconcilableobject_getprogressfeedbackmaxestimate
req.header: reconcil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IReconcilableObject::GetProgressFeedbackMaxEstimate
 - reconcil/IReconcilableObject::GetProgressFeedbackMaxEstimate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IReconcilableObject.GetProgressFeedbackMaxEstimate
---

# IReconcilableObject::GetProgressFeedbackMaxEstimate


## -description

Retrieves an estimated measurement of the amount of work required to complete a reconciliation. Reconcilers typically use this method to estimate the work needed to reconcile an embedded document. This value corresponds to a similar value that is passed with the <a href="/previous-versions/bb761347(v=vs.85)">SetProgressFeedback</a> method during reconciliation.

## -parameters

### -param pulProgressMax

Type: <b>ULONG*</b>

The address of the variable to receive the work estimate value.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or one of the following error values otherwise.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The object is an OLE embedded document that must be run before this operation can be carried out. The object state is unchanged as a result of the call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/reconcil/nn-reconcil-ireconcilableobject">IReconcilableObject</a>