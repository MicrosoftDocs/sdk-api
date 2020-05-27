---
UID: NN:propsys.IDelayedPropertyStoreFactory
title: IDelayedPropertyStoreFactory (propsys.h)
description: Exposes a method to create a specified IPropertyStore object in circumstances where property access is potentially slow.
helpviewer_keywords: ["IDelayedPropertyStoreFactory","IDelayedPropertyStoreFactory interface [Windows Shell]","IDelayedPropertyStoreFactory interface [Windows Shell]","described","_shell_IDelayedPropertyStoreFactory","propsys/IDelayedPropertyStoreFactory","shell.IDelayedPropertyStoreFactory"]
old-location: shell\IDelayedPropertyStoreFactory.htm
tech.root: shell
ms.assetid: 855c9f10-9f40-4c60-a669-551fa51133f5
ms.date: 12/05/2018
ms.keywords: IDelayedPropertyStoreFactory, IDelayedPropertyStoreFactory interface [Windows Shell], IDelayedPropertyStoreFactory interface [Windows Shell],described, _shell_IDelayedPropertyStoreFactory, propsys/IDelayedPropertyStoreFactory, shell.IDelayedPropertyStoreFactory
f1_keywords:
- propsys/IDelayedPropertyStoreFactory
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
- IDelayedPropertyStoreFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDelayedPropertyStoreFactory interface


## -description


Exposes a method to create a specified <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object in circumstances where property access is potentially slow.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDelayedPropertyStoreFactory</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystorefactory">IPropertyStoreFactory</a>. <b>IDelayedPropertyStoreFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDelayedPropertyStoreFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-idelayedpropertystorefactory-getdelayedpropertystore">GetDelayedPropertyStore</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface object, as specified.

</td>
</tr>
</table> 

