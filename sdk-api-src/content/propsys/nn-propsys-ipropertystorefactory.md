---
UID: NN:propsys.IPropertyStoreFactory
title: IPropertyStoreFactory (propsys.h)
description: Exposes methods to get an IPropertyStore object.
old-location: properties\IPropertyStoreFactory.htm
tech.root: properties
ms.assetid: 78ea822d-da8e-4883-b0eb-4277e7eb87a2
ms.date: 12/05/2018
ms.keywords: IPropertyStoreFactory, IPropertyStoreFactory interface [Windows Properties], IPropertyStoreFactory interface [Windows Properties],described, _shell_IPropertyStoreFactory, properties.IPropertyStoreFactory, propsys/IPropertyStoreFactory, shell.IPropertyStoreFactory
ms.topic: interface
f1_keywords:
- propsys/IPropertyStoreFactory
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Propsys.h
api_name:
- IPropertyStoreFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyStoreFactory interface


## -description


Exposes methods to get an <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyStoreFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyStoreFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyStoreFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore">GetPropertyStore</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object that corresponds to the supplied flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystorefactory-getpropertystoreforkeys">GetPropertyStoreForKeys</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object, given a set of property keys. This provides an alternative, possibly faster, method of getting an <b>IPropertyStore</b> object compared to calling <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore">IPropertyStoreFactory::GetPropertyStore</a>.

</td>
</tr>
</table> 


## -remarks



This interface is typically obtained through <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a> or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler">IShellItem::BindToHandler</a>. It is useful for data source implementers who want to avoid the additional overhead of creating a property store through <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a>. However, <b>IShellItem2::GetPropertyStore</b> is the recommended method to obtain a property store unless you are implementing a data source through a Shell folder extension.
            




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pscreatepropertystorefromobject">PSCreatePropertyStoreFromObject</a>
 

 

