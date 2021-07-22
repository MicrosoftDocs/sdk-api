---
UID: NN:shobjidl_core.IParentAndItem
title: IParentAndItem (shobjidl_core.h)
description: Exposes methods that get and set the parent and the parent's child ID. While IParentAndItem is typically implemented on IShellItems, it is not specific to IShellItem.
helpviewer_keywords: ["IParentAndItem","IParentAndItem interface [Windows Shell]","IParentAndItem interface [Windows Shell]","described","_shell_IParentAndItem","shell.IParentAndItem","shobjidl_core/IParentAndItem"]
old-location: shell\IParentAndItem.htm
tech.root: shell
ms.assetid: 5cca426f-73fb-4b39-8eb0-16c01673c311
ms.date: 12/05/2018
ms.keywords: IParentAndItem, IParentAndItem interface [Windows Shell], IParentAndItem interface [Windows Shell],described, _shell_IParentAndItem, shell.IParentAndItem, shobjidl_core/IParentAndItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - IParentAndItem
 - shobjidl_core/IParentAndItem
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
 - IParentAndItem
---

# IParentAndItem interface


## -description

Exposes methods that get and set the parent and the parent's child ID. While <b>IParentAndItem</b> is typically implemented on IShellItems, it is not specific to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

## -inheritance

The <b>IParentAndItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IParentAndItem</b> also has these types of members:

## -remarks

The performance improvement using this interface can be noted in comparison with <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist">IPersistIDList</a>, an interface that uses absolute item identifier lists. Subsequent operations on objects that implement <b>IPersistIDList</b> may require <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a> calls, and these calls may impact performance.  In the case of IShellItems and participating IShellFolders that implement <b>IParentAndItem</b>, the parent <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> may already be cached. By implementing <b>IParentAndItem</b> and then getting/setting the parent <b>IShellFolder</b> directly, the call to <b>IShellFolder::BindToObject</b> on the item identifier list to retrieve the <b>IShellFolder</b> interface is eliminated.
