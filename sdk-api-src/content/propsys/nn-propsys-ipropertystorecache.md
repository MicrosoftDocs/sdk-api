---
UID: NN:propsys.IPropertyStoreCache
title: IPropertyStoreCache (propsys.h)
description: Exposes methods that allow a handler to manage various states for each property.
helpviewer_keywords: ["IPropertyStoreCache","IPropertyStoreCache interface [Windows Properties]","IPropertyStoreCache interface [Windows Properties]","described","properties.IPropertyStoreCache","propsys/IPropertyStoreCache","shell.IPropertyStoreCache","shell_IPropertyStoreCache"]
old-location: properties\IPropertyStoreCache.htm
tech.root: properties
ms.assetid: ac4f7e3b-6702-4239-b248-0645d961fbf8
ms.date: 12/05/2018
ms.keywords: IPropertyStoreCache, IPropertyStoreCache interface [Windows Properties], IPropertyStoreCache interface [Windows Properties],described, properties.IPropertyStoreCache, propsys/IPropertyStoreCache, shell.IPropertyStoreCache, shell_IPropertyStoreCache
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
 - IPropertyStoreCache
 - propsys/IPropertyStoreCache
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
 - IPropertyStoreCache
---

# IPropertyStoreCache interface


## -description

Exposes methods that allow a handler to manage various states for each property.

## -inheritance

The <b>IPropertyStoreCache</b> interface inherits from <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>. <b>IPropertyStoreCache</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided by CLSID_InMemoryPropertyStore. Users should never need to implement it themselves.

                

CLSID_InMemoryPropertyStore implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystorecache">IPropertyStoreCache</a> as well as <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> and other interfaces so that it can store additional information (<a href="/windows/desktop/api/propsys/ne-propsys-psc_state">PSC_STATE</a>) about each of the properties. This information can be useful for property handler implementers. It can also be useful in other scenarios where a cache of property values is needed.
