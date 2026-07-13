---
UID: NN:shobjidl_core.IShellItem
title: IShellItem (shobjidl_core.h)
description: Exposes methods that retrieve information about a Shell item. IShellItem and IShellItem2 are the preferred representations of items in any new code.
helpviewer_keywords: ["IShellItem","IShellItem interface [Windows Shell]","IShellItem interface [Windows Shell]","described","_win32_IShellItem","shell.IShellItem","shobjidl_core/IShellItem"]
old-location: shell\IShellItem.htm
tech.root: shell
ms.assetid: 599b9c0a-df04-4dbd-a5a6-a8736eecc560
ms.date: 12/05/2018
ms.keywords: IShellItem, IShellItem interface [Windows Shell], IShellItem interface [Windows Shell],described, _win32_IShellItem, shell.IShellItem, shobjidl_core/IShellItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItem
 - shobjidl_core/IShellItem
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
 - IShellItem
---

# IShellItem interface


## -description

Exposes methods that retrieve information about a Shell item. <b>IShellItem</b> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2">IShellItem2</a> are the preferred representations of items in any new code.

## -inheritance

The <b>IShellItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellItem</b> also has these types of members:
<ul>
<li><a href="/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem#methods">Methods</a></li>
</ul>

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Third parties do not implement this interface; only use the implementation provided with the system.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2">IShellItem2</a>
