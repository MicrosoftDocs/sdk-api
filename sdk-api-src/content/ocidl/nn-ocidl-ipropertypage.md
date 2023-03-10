---
UID: NN:ocidl.IPropertyPage
title: IPropertyPage (ocidl.h)
description: Provides the main features of a property page object that manages a particular page within a property sheet.
helpviewer_keywords: ["IPropertyPage","IPropertyPage interface [COM]","IPropertyPage interface [COM]","described","_ctrl_ipropertypage","com.ipropertypage","ocidl/IPropertyPage"]
old-location: com\ipropertypage.htm
tech.root: com
ms.assetid: ad2cb3ae-dd24-4774-95bd-f5a0773c68b1
ms.date: 12/05/2018
ms.keywords: IPropertyPage, IPropertyPage interface [COM], IPropertyPage interface [COM],described, _ctrl_ipropertypage, com.ipropertypage, ocidl/IPropertyPage
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
 - IPropertyPage
 - ocidl/IPropertyPage
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
 - IPropertyPage
---

# IPropertyPage interface


## -description

Provides the main features of a property page object that manages a particular page within a property sheet. A property page implements at least <b>IPropertyPage</b> and can optionally implement <a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a> if selection of a specific property is supported. See <a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-mappropertytopage">IPerPropertyBrowsing::MapPropertyToPage</a> for more information on specific property browsing. The methods of <b>IPropertyPage2</b> enable the property sheet or property frame to instruct the page when to perform specific actions, mostly based on user input such as switching between pages or pressing various buttons that the frame itself manages in the dialog box.

A property page manages a dialog box that contains only those controls that should be displayed for that one page within the property sheet itself. This means that the dialog box template used to define the page should only carry the WS_CHILD style and no others. It should not include any style related to a frame, caption, or system menus or controls.

## -inheritance

The <b>IPropertyPage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyPage</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iperpropertybrowsing">IPerPropertyBrowsing</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ispecifypropertypages">ISpecifyPropertyPage</a>



<a href="/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframe">OleCreatePropertyFrame</a>



<a href="/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframeindirect">OleCreatePropertyFrameIndirect</a>
