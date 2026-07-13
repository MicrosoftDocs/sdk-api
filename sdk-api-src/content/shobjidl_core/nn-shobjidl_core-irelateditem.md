---
UID: NN:shobjidl_core.IRelatedItem
title: IRelatedItem (shobjidl_core.h)
description: Exposes methods that derive related items with specific relationships.
helpviewer_keywords: ["IRelatedItem","IRelatedItem interface [Windows Shell]","IRelatedItem interface [Windows Shell]","described","_shell_IRelatedItem","shell.IRelatedItem","shobjidl_core/IRelatedItem"]
old-location: shell\IRelatedItem.htm
tech.root: shell
ms.assetid: f42d218c-0251-45e0-b05a-f1ccdcaf036c
ms.date: 12/05/2018
ms.keywords: IRelatedItem, IRelatedItem interface [Windows Shell], IRelatedItem interface [Windows Shell],described, _shell_IRelatedItem, shell.IRelatedItem, shobjidl_core/IRelatedItem
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
 - IRelatedItem
 - shobjidl_core/IRelatedItem
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
 - IRelatedItem
---

# IRelatedItem interface


## -description

Exposes methods that derive related items with specific relationships.

## -inheritance

The <b>IRelatedItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRelatedItem</b> also has these types of members:

## -remarks

Do not implement this interface directly. This is a base interface (other interfaces derive from it) for a set of interfaces that describes the relationship between two items, (For example <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idisplayitem">IDisplayItem</a>).  Do not query for this interface directly, for example, using <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a>. Instead, use the derived interfaces.

An example derivation is the creation of an identity name handler. For more information, see <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iidentityname">IIdentityName</a>. Other interfaces that may derive from this interface include <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icurrentitem">ICurrentItem</a>, and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfermediumitem">ITransferMediumItem</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler">IShellItem::BindToHandler</a>
