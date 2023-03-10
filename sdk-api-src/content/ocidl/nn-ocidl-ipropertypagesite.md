---
UID: NN:ocidl.IPropertyPageSite
title: IPropertyPageSite (ocidl.h)
description: Provides the main features for a property page site object.
helpviewer_keywords: ["IPropertyPageSite","IPropertyPageSite interface [COM]","IPropertyPageSite interface [COM]","described","_ctrl_ipropertypagesite","com.ipropertypagesite","ocidl/IPropertyPageSite"]
old-location: com\ipropertypagesite.htm
tech.root: com
ms.assetid: a9035a10-2078-4626-8386-f9298526dfb7
ms.date: 12/05/2018
ms.keywords: IPropertyPageSite, IPropertyPageSite interface [COM], IPropertyPageSite interface [COM],described, _ctrl_ipropertypagesite, com.ipropertypagesite, ocidl/IPropertyPageSite
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
 - IPropertyPageSite
 - ocidl/IPropertyPageSite
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
 - IPropertyPageSite
---

# IPropertyPageSite interface


## -description

Provides the main features for a property page site object.

## -inheritance

The <b>IPropertyPageSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyPageSite</b> also has these types of members:

## -remarks

For each property page created within a property frame, the frame creates a property page site to provide information to the property page and to receive notifications from the page when changes occur. This latter notification is used to initiate a call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-ispagedirty">IPropertyPage::IsPageDirty</a>, the return value of which is then used to enable or disable the frame's <b>Apply</b> button.

<h3><a id="OLE_Implementation"></a><a id="ole_implementation"></a><a id="OLE_IMPLEMENTATION"></a>OLE Implementation</h3>
The system provides an implementation of the <b>IPropertyPageSite</b> interface through the <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframe">OleCreatePropertyFrame</a> or <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframeindirect">OleCreatePropertyFrameIndirect</a> functions. The frame implementation provided through these functions only implements the <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-onstatuschange">OnStatusChange</a> and <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getlocaleid">GetLocaleID</a> methods. The <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getpagecontainer">GetPageContainer</a> and <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-translateaccelerator">TranslateAccelerator</a> methods return E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iperpropertybrowsing">IPerPropertyBrowsing</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ispecifypropertypages">ISpecifyPropertyPage</a>
