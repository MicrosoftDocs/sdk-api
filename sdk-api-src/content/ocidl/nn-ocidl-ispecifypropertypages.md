---
UID: NN:ocidl.ISpecifyPropertyPages
title: ISpecifyPropertyPages (ocidl.h)
description: Indicates that an object supports property pages.
helpviewer_keywords: ["ISpecifyPropertyPages","ISpecifyPropertyPages interface [COM]","ISpecifyPropertyPages interface [COM]","described","_ctrl_ispecifypropertypages","com.ispecifypropertypages","ocidl/ISpecifyPropertyPages"]
old-location: com\ispecifypropertypages.htm
tech.root: com
ms.assetid: fd986241-aabe-477e-a382-28a1ecfd5410
ms.date: 12/05/2018
ms.keywords: ISpecifyPropertyPages, ISpecifyPropertyPages interface [COM], ISpecifyPropertyPages interface [COM],described, _ctrl_ispecifypropertypages, com.ispecifypropertypages, ocidl/ISpecifyPropertyPages
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpecifyPropertyPages
 - ocidl/ISpecifyPropertyPages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - ISpecifyPropertyPages
---

# ISpecifyPropertyPages interface


## -description

Indicates that an object supports property pages. OLE property pages enable an object to display its properties in a tabbed dialog box known as a <i>property sheet</i>. An end user can then view and change the object's properties. An object can display its property pages independent of its client, or the client can manage the display of property pages from a number of contained objects in a single property sheet. Property pages also provide a means for notifying a client of changes in an object's properties.

## -inheritance

The <b>ISpecifyPropertyPages</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpecifyPropertyPages</b> also has these types of members:

## -remarks

 A property page object manages a particular page within a property sheet. A property page implements at least <a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a> and can optionally implement <a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a> if selection of a specific property is supported.

An object specifies its support for property pages by implementing <b>ISpecifyPropertyPages</b>. Through this interface the caller can obtain a list of CLSIDs identifying the specific property pages that the object supports. If the object specifies a property page CLSID, the object must be able to receive property changes from the property page.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a>
