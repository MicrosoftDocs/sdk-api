---
UID: NN:propsys.IPropertyStoreFactory
title: IPropertyStoreFactory (propsys.h)
description: Exposes methods to get an IPropertyStore object.
helpviewer_keywords: ["IPropertyStoreFactory","IPropertyStoreFactory interface [Windows Properties]","IPropertyStoreFactory interface [Windows Properties]","described","_shell_IPropertyStoreFactory","properties.IPropertyStoreFactory","propsys/IPropertyStoreFactory","shell.IPropertyStoreFactory"]
old-location: properties\IPropertyStoreFactory.htm
tech.root: properties
ms.assetid: 78ea822d-da8e-4883-b0eb-4277e7eb87a2
ms.date: 12/05/2018
ms.keywords: IPropertyStoreFactory, IPropertyStoreFactory interface [Windows Properties], IPropertyStoreFactory interface [Windows Properties],described, _shell_IPropertyStoreFactory, properties.IPropertyStoreFactory, propsys/IPropertyStoreFactory, shell.IPropertyStoreFactory
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IPropertyStoreFactory
 - propsys/IPropertyStoreFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyStoreFactory
---

# IPropertyStoreFactory interface


## -description

Exposes methods to get an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object.

## -inheritance

The <b>IPropertyStoreFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyStoreFactory</b> also has these types of members:

## -remarks

This interface is typically obtained through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler">IShellItem::BindToHandler</a>. It is useful for data source implementers who want to avoid the additional overhead of creating a property store through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a>. However, <b>IShellItem2::GetPropertyStore</b> is the recommended method to obtain a property store unless you are implementing a data source through a Shell folder extension.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pscreatepropertystorefromobject">PSCreatePropertyStoreFromObject</a>
