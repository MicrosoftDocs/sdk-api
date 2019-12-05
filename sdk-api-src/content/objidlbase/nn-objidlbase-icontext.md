---
UID: NN:objidlbase.IContext
title: IContext (objidlbase.h)
description: Supports setting COM+ context properties.
old-location: com\icontext.htm
tech.root: com
ms.assetid: 89c41d9c-186c-4927-990d-92aa501f7d35
ms.date: 12/05/2018
ms.keywords: IContext, IContext interface [COM], IContext interface [COM],described, _com_icontext, com.icontext, objidlbase/IContext
ms.topic: interface
f1_keywords:
- objidlbase/IContext
dev_langs:
- c++
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
- objidlbase.h
api_name:
- IContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContext interface


## -description


Supports setting COM+ context properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icontext-enumcontextprops">EnumContextProps</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumcontextprops">IEnumContextProps</a> interface pointer that can be used to enumerate the context properties in this context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icontext-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the specified context property from the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icontext-removeproperty">RemoveProperty</a>
</td>
<td align="left" width="63%">
Removes the specified context property from the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icontext-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Adds the specified context property to the object context.

</td>
</tr>
</table> 


## -remarks



 An instance of this interface for the current context can be obtained using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetobjectcontext">CoGetObjectContext</a>.



