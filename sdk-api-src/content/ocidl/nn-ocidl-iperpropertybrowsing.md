---
UID: NN:ocidl.IPerPropertyBrowsing
title: IPerPropertyBrowsing (ocidl.h)
description: Retrieves the information in the property pages offered by an object.
old-location: com\iperpropertybrowsing.htm
tech.root: com
ms.assetid: 05e46df3-b6c8-4520-af11-21e1ff90fb9f
ms.date: 12/05/2018
ms.keywords: IPerPropertyBrowsing, IPerPropertyBrowsing interface [COM], IPerPropertyBrowsing interface [COM],described, _ctrl_iperpropertybrowsing, com.iperpropertybrowsing, ocidl/IPerPropertyBrowsing
ms.topic: interface
f1_keywords:
- ocidl/IPerPropertyBrowsing
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
- IPerPropertyBrowsing
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPerPropertyBrowsing interface


## -description


Retrieves the information in the property pages offered by an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPerPropertyBrowsing</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPerPropertyBrowsing</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPerPropertyBrowsing</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getdisplaystring">GetDisplayString</a>
</td>
<td align="left" width="63%">
Retrieves a text string describing the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings">GetPredefinedStrings</a>
</td>
<td align="left" width="63%">
Retrieves an array description strings for the allowable values that the specified property can accept.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue">GetPredefinedValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified property that is associated with a predefined string name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-mappropertytopage">MapPropertyToPage</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of the property page associated with the specified property.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ispecifypropertypages">ISpecifyPropertyPage</a>
 

 

