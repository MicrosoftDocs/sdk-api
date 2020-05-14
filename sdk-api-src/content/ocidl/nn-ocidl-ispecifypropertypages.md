---
UID: NN:ocidl.ISpecifyPropertyPages
title: ISpecifyPropertyPages (ocidl.h)
description: Indicates that an object supports property pages.helpviewer_keywords: ["ISpecifyPropertyPages","ISpecifyPropertyPages interface [COM]","ISpecifyPropertyPages interface [COM]","described","_ctrl_ispecifypropertypages","com.ispecifypropertypages","ocidl/ISpecifyPropertyPages"]
old-location: com\ispecifypropertypages.htm
tech.root: com
ms.assetid: fd986241-aabe-477e-a382-28a1ecfd5410
ms.date: 12/05/2018
ms.keywords: ISpecifyPropertyPages, ISpecifyPropertyPages interface [COM], ISpecifyPropertyPages interface [COM],described, _ctrl_ispecifypropertypages, com.ispecifypropertypages, ocidl/ISpecifyPropertyPages
f1_keywords:
- ocidl/ISpecifyPropertyPages
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
- ISpecifyPropertyPages
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpecifyPropertyPages interface


## -description


Indicates that an object supports property pages. OLE property pages enable an object to display its properties in a tabbed dialog box known as a <i>property sheet</i>. An end user can then view and change the object's properties. An object can display its property pages independent of its client, or the client can manage the display of property pages from a number of contained objects in a single property sheet. Property pages also provide a means for notifying a client of changes in an object's properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpecifyPropertyPages</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpecifyPropertyPages</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpecifyPropertyPages</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ispecifypropertypages-getpages">GetPages</a>
</td>
<td align="left" width="63%">
Retrieves a list of property pages that can be displayed in this object's property sheet.

</td>
</tr>
</table> 


## -remarks



 A property page object manages a particular page within a property sheet. A property page implements at least <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a> and can optionally implement <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a> if selection of a specific property is supported.

An object specifies its support for property pages by implementing <b>ISpecifyPropertyPages</b>. Through this interface the caller can obtain a list of CLSIDs identifying the specific property pages that the object supports. If the object specifies a property page CLSID, the object must be able to receive property changes from the property page.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a>
 

 

