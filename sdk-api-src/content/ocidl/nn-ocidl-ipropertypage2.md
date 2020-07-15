---
UID: NN:ocidl.IPropertyPage2
title: IPropertyPage2 (ocidl.h)
description: An extension to IPropertyPage to support initial selection of a property on a page.
helpviewer_keywords: ["IPropertyPage2","IPropertyPage2 interface [COM]","IPropertyPage2 interface [COM]","described","_ctrl_ipropertypage2","com.ipropertypage2","ocidl/IPropertyPage2"]
old-location: com\ipropertypage2.htm
tech.root: com
ms.assetid: 65cd8f97-f88c-433c-b4e7-9dace7193ec1
ms.date: 12/05/2018
ms.keywords: IPropertyPage2, IPropertyPage2 interface [COM], IPropertyPage2 interface [COM],described, _ctrl_ipropertypage2, com.ipropertypage2, ocidl/IPropertyPage2
f1_keywords:
- ocidl/IPropertyPage2
dev_langs:
- c++
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
- OCIdl.h
api_name:
- IPropertyPage2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyPage2 interface


## -description


An extension to <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a> to support initial selection of a property on a page.

This method works in conjunction with the implementation of <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-mappropertytopage">IPerPropertyBrowsing::MapPropertyToPage</a> on an object that supplies properties and specifies property pages through <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ispecifypropertypages">ISpecifyPropertyPages</a>. This interface has only one extra method in addition to those in <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>. That method, <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage2-editproperty">IPropertyPage2::EditProperty</a> tells the page which property to highlight.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyPage2</b> interface inherits from <b>IPropertyPage</b>. <b>IPropertyPage2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyPage2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage2-editproperty">EditProperty</a>
</td>
<td align="left" width="63%">
Specifies which field is to receive the focus when the property page is activated.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iperpropertybrowsing">IPerPropertyBrowsing</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ispecifypropertypages">ISpecifyPropertyPage</a>
 

 

