---
UID: NN:reconcil.IReconcilableObject
title: IReconcilableObject (reconcil.h)
description: Exposes methods that reconcile a given document. The briefcase reconciler is responsible for implementing this interface.
helpviewer_keywords: ["IReconcilableObject","IReconcilableObject interface [Legacy Windows Environment Features]","IReconcilableObject interface [Legacy Windows Environment Features]","described","_win32_IReconcilableObject","lwef.ireconcilableobject","reconcil/IReconcilableObject","shell.ireconcilableobject"]
old-location: lwef\ireconcilableobject.htm
tech.root: lwef
ms.assetid: 2a0ec2c0-0bec-4aeb-bbd5-0db18f0d5f8c
ms.date: 12/05/2018
ms.keywords: IReconcilableObject, IReconcilableObject interface [Legacy Windows Environment Features], IReconcilableObject interface [Legacy Windows Environment Features],described, _win32_IReconcilableObject, lwef.ireconcilableobject, reconcil/IReconcilableObject, shell.ireconcilableobject
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
 - IReconcilableObject
 - reconcil/IReconcilableObject
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
 - IReconcilableObject
---

# IReconcilableObject interface


## -description

Exposes methods that reconcile a given document. The briefcase reconciler is responsible for implementing this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReconcilableObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReconcilableObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReconcilableObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate">GetProgressFeedbackMaxEstimate</a>
</td>
<td align="left" width="63%">
Retrieves an estimated measurement of the amount of work required to complete a reconciliation. Reconcilers typically use this method to estimate the work needed to reconcile an embedded document. This value corresponds to a similar value that is passed with the <a href="/previous-versions/bb761347(v=vs.85)">IReconcileInitiator::SetProgressFeedback</a> method during reconciliation. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/reconcil/nf-reconcil-ireconcilableobject-reconcile">Reconcile</a>
</td>
<td align="left" width="63%">
Reconciles the state of an object with one or more other objects. The reconciliation updates the internal state of the object by merging the states of all objects to form a combined state. 

</td>
</tr>
</table>