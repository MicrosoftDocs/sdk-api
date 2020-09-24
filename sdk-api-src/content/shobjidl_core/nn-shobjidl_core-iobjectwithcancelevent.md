---
UID: NN:shobjidl_core.IObjectWithCancelEvent
title: IObjectWithCancelEvent (shobjidl_core.h)
description: Not supported.Supplies a caller with an event that will be signaled by the called object to denote cancellation of a task.
helpviewer_keywords: ["IObjectWithCancelEvent","IObjectWithCancelEvent interface [Windows Shell]","IObjectWithCancelEvent interface [Windows Shell]","described","_shell_IObjectWithCancelEvent","shell.IObjectWithCancelEvent","shobjidl_core/IObjectWithCancelEvent"]
old-location: shell\IObjectWithCancelEvent.htm
tech.root: shell
ms.assetid: 3bac219d-d9fd-4259-8f34-032554291327
ms.date: 12/05/2018
ms.keywords: IObjectWithCancelEvent, IObjectWithCancelEvent interface [Windows Shell], IObjectWithCancelEvent interface [Windows Shell],described, _shell_IObjectWithCancelEvent, shell.IObjectWithCancelEvent, shobjidl_core/IObjectWithCancelEvent
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IObjectWithCancelEvent
 - shobjidl_core/IObjectWithCancelEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IObjectWithCancelEvent
---

# IObjectWithCancelEvent interface


## -description

Not supported.

Supplies a caller with an event that will be signaled by the called object to denote cancellation of a task.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectWithCancelEvent</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectWithCancelEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectWithCancelEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithcancelevent-getcancelevent">GetCancelEvent</a>
</td>
<td align="left" width="63%">
Retrieves an event that will be sent when an operation is cancelled.

</td>
</tr>
</table>