---
UID: NN:reconcil.INotifyReplica
title: INotifyReplica (reconcil.h)
description: Exposes a method that provides an object's creator with the means to notify the object that it may be subject to subsequent reconciliation. The briefcase reconciler is responsible for implementing this interface.
helpviewer_keywords: ["INotifyReplica","INotifyReplica interface [Windows Shell]","INotifyReplica interface [Windows Shell]","described","_win32_INotifyReplica","reconcil/INotifyReplica","shell.INotifyReplica"]
old-location: shell\INotifyReplica.htm
tech.root: shell
ms.assetid: aa04d5b0-8483-4024-91d0-65d69d6891ca
ms.date: 12/05/2018
ms.keywords: INotifyReplica, INotifyReplica interface [Windows Shell], INotifyReplica interface [Windows Shell],described, _win32_INotifyReplica, reconcil/INotifyReplica, shell.INotifyReplica
f1_keywords:
- reconcil/INotifyReplica
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
- INotifyReplica
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INotifyReplica interface


## -description


Exposes a method that provides an object's creator with the means to notify the object that it may be subject to subsequent reconciliation. The briefcase reconciler is responsible for implementing this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INotifyReplica</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INotifyReplica</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INotifyReplica</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica">YouAreAReplica</a>
</td>
<td align="left" width="63%">
Notifies an object that it may be subject to subsequent reconciliation through the <a href="https://docs.microsoft.com/windows/desktop/api/reconcil/nf-reconcil-ireconcilableobject-reconcile">IReconcilableObject::Reconcile</a> method.

</td>
</tr>
</table> 

