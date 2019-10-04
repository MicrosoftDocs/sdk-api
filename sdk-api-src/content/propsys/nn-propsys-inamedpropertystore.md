---
UID: NN:propsys.INamedPropertyStore
title: INamedPropertyStore (propsys.h)
author: windows-sdk-content
description: Exposes methods that get and set named properties.
old-location: shell\INamedPropertyStore.htm
tech.root: shell
ms.assetid: 5f7997ba-a5c8-42b5-90c8-5cb34afd6092
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INamedPropertyStore, INamedPropertyStore interface [Windows Shell], INamedPropertyStore interface [Windows Shell],described, _shell_INamedPropertyStore, propsys/INamedPropertyStore, shell.INamedPropertyStore
ms.topic: interface
f1_keywords: 
 - "propsys/INamedPropertyStore"
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
 - INamedPropertyStore
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INamedPropertyStore interface


## -description


Exposes methods that get and set named properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INamedPropertyStore</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INamedPropertyStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INamedPropertyStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-inamedpropertystore-getnameat">GetNameAt</a>
</td>
<td align="left" width="63%">
Gets the name of a property at a specified index in the property store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-inamedpropertystore-getnamecount">GetNameCount</a>
</td>
<td align="left" width="63%">
Gets the number of property names in the property store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-inamedpropertystore-getnamedvalue">GetNamedValue</a>
</td>
<td align="left" width="63%">
Gets the value of a named property from the named property store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-inamedpropertystore-setnamedvalue">SetNamedValue</a>
</td>
<td align="left" width="63%">
Sets the value of a named property.

</td>
</tr>
</table> 

