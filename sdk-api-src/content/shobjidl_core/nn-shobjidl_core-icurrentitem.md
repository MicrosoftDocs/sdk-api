---
UID: NN:shobjidl_core.ICurrentItem
title: ICurrentItem (shobjidl_core.h)
description: Obtained by calling IShellFolder::BindToObject for an item. If the item represents a snapshot of an item at a previous time, this interface will obtain the current version of the item.
helpviewer_keywords: ["ICurrentItem","ICurrentItem interface [Windows Shell]","ICurrentItem interface [Windows Shell]","described","_shell_ICurrentItem","shell.ICurrentItem","shobjidl_core/ICurrentItem"]
old-location: shell\ICurrentItem.htm
tech.root: shell
ms.assetid: a5ff7199-134d-4c1a-91e0-a81ff474f5a6
ms.date: 12/05/2018
ms.keywords: ICurrentItem, ICurrentItem interface [Windows Shell], ICurrentItem interface [Windows Shell],described, _shell_ICurrentItem, shell.ICurrentItem, shobjidl_core/ICurrentItem
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ICurrentItem
 - shobjidl_core/ICurrentItem
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
 - ICurrentItem
---

# ICurrentItem interface


## -description

Obtained by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a> for an item. If the item represents a snapshot of an item at a previous time, this interface will obtain the current version of the item.

## -remarks

This interface provides only the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem">IRelatedItem</a> interface, from which it inherits.