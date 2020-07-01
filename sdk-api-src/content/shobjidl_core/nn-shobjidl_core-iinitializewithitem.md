---
UID: NN:shobjidl_core.IInitializeWithItem
title: IInitializeWithItem (shobjidl_core.h)
description: Exposes a method used to initialize a handler, such as a property handler, thumbnail handler, or preview handler, with an IShellItem.
helpviewer_keywords: ["IInitializeWithItem","IInitializeWithItem interface [Windows Shell]","IInitializeWithItem interface [Windows Shell]","described","shell.IInitializeWithItem","shell_IInitializeWithItem","shobjidl_core/IInitializeWithItem"]
old-location: shell\IInitializeWithItem.htm
tech.root: shell
ms.assetid: 95f3917e-66ca-45de-a3ed-811680a179e7
ms.date: 12/05/2018
ms.keywords: IInitializeWithItem, IInitializeWithItem interface [Windows Shell], IInitializeWithItem interface [Windows Shell],described, shell.IInitializeWithItem, shell_IInitializeWithItem, shobjidl_core/IInitializeWithItem
f1_keywords:
- shobjidl_core/IInitializeWithItem
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
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
- shobjidl_core.h
api_name:
- IInitializeWithItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInitializeWithItem interface


## -description


Exposes a method used to initialize a handler, such as a property handler, thumbnail handler, or preview handler, with an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitializeWithItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInitializeWithItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInitializeWithItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a handler with an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

</td>
</tr>
</table> 


## -remarks



Whenever possible, it is recommended that initialization be done through a stream using <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-iinitializewithstream">IInitializeWithStream</a>. Benefits of this include increased security and stability.



