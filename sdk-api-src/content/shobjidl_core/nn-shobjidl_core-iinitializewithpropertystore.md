---
UID: NN:shobjidl_core.IInitializeWithPropertyStore
title: IInitializeWithPropertyStore (shobjidl_core.h)
description: Exposes a method that initializes a handler, such as a property handler, thumbnail handler, or preview handler, with a property store.
helpviewer_keywords: ["IInitializeWithPropertyStore","IInitializeWithPropertyStore interface [Windows Shell]","IInitializeWithPropertyStore interface [Windows Shell]","described","_shell_IInitializeWithPropertyStore","shell.IInitializeWithPropertyStore","shobjidl_core/IInitializeWithPropertyStore"]
old-location: shell\IInitializeWithPropertyStore.htm
tech.root: shell
ms.assetid: da8592a9-7727-433f-ac92-abf22a735eb2
ms.date: 12/05/2018
ms.keywords: IInitializeWithPropertyStore, IInitializeWithPropertyStore interface [Windows Shell], IInitializeWithPropertyStore interface [Windows Shell],described, _shell_IInitializeWithPropertyStore, shell.IInitializeWithPropertyStore, shobjidl_core/IInitializeWithPropertyStore
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
 - IInitializeWithPropertyStore
 - shobjidl_core/IInitializeWithPropertyStore
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
 - IInitializeWithPropertyStore
---

# IInitializeWithPropertyStore interface


## -description

Exposes a method that initializes a handler, such as a property handler, thumbnail handler, or preview handler, with a property store.

## -inheritance

The <b>IInitializeWithPropertyStore</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInitializeWithPropertyStore</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Use this interface when initializing a handler for OpenSearch result sets, which are returned as RSS or Atom feeds.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithpropertystore">IInitializeWithPropertyStore</a>



<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>
