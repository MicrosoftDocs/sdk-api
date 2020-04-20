---
UID: NN:propsys.IPropertyChange
title: IPropertyChange (propsys.h)
description: Exposes a method that encapsulates a change to a single property.helpviewer_keywords: ["IPropertyChange","IPropertyChange interface [Windows Properties]","IPropertyChange interface [Windows Properties]","described","_shell_IPropertyChange","properties.IPropertyChange","propsys/IPropertyChange","shell.IPropertyChange"]
old-location: properties\IPropertyChange.htm
tech.root: properties
ms.assetid: 7bdc31d8-ba03-4010-8aa1-89701ebbf8cd
ms.date: 12/05/2018
ms.keywords: IPropertyChange, IPropertyChange interface [Windows Properties], IPropertyChange interface [Windows Properties],described, _shell_IPropertyChange, properties.IPropertyChange, propsys/IPropertyChange, shell.IPropertyChange
f1_keywords:
- propsys/IPropertyChange
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
- IPropertyChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyChange interface


## -description


Exposes a method that encapsulates a change to a single property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyChange</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-iobjectwithpropertykey">IObjectWithPropertyKey</a>. <b>IPropertyChange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyChange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertychange-applytopropvariant">ApplyToPropVariant</a>
</td>
<td align="left" width="63%">
Applies a change to a property value.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-iobjectwithpropertykey">IObjectWithPropertyKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pscreatesimplepropertychange">PSCreateSimplePropertyChange</a>
 

 

