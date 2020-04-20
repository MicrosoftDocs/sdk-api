---
UID: NN:reconcil.IReconcileInitiator
title: IReconcileInitiator (reconcil.h)
description: Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document. The initiator is responsible for implementing this interface.helpviewer_keywords: ["IReconcileInitiator","IReconcileInitiator interface [Legacy Windows Environment Features]","IReconcileInitiator interface [Legacy Windows Environment Features]","described","_win32_IReconcileInitiator","lwef.ireconcileinitiator","reconcil/IReconcileInitiator","shell.ireconcileinitiator"]
old-location: lwef\ireconcileinitiator.htm
tech.root: lwef
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
ms.date: 12/05/2018
ms.keywords: IReconcileInitiator, IReconcileInitiator interface [Legacy Windows Environment Features], IReconcileInitiator interface [Legacy Windows Environment Features],described, _win32_IReconcileInitiator, lwef.ireconcileinitiator, reconcil/IReconcileInitiator, shell.ireconcileinitiator
f1_keywords:
- reconcil/IReconcileInitiator
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IReconcileInitiator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReconcileInitiator interface


## -description


Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document. The initiator is responsible for implementing this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IReconcileInitiator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReconcileInitiator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IReconcileInitiator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/bb761345(v=vs.85)">SetAbortCallback</a>
</td>
<td align="left" width="63%">
Sets the object through which the initiator can asynchronously terminate a reconciliation. A briefcase reconciler typically sets this object for reconciliations that are lengthy or involve user interaction. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/bb761347(v=vs.85)">SetProgressFeedback</a>
</td>
<td align="left" width="63%">
Indicates the amount of progress the briefcase reconciler has made toward completing the reconciliation. The amount is a fraction and is computed as the quotient of the <i>ulProgress</i> and <i>ulProgressMax</i> parameters. Reconcilers should call this method periodically during their reconciliation process. 

</td>
</tr>
</table> 

