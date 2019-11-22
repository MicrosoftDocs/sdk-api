---
UID: NN:ocidl.IPropertyPageSite
title: IPropertyPageSite (ocidl.h)

description: Provides the main features for a property page site object.
old-location: com\ipropertypagesite.htm
tech.root: com
ms.assetid: a9035a10-2078-4626-8386-f9298526dfb7

ms.date: 12/05/2018
ms.keywords: IPropertyPageSite, IPropertyPageSite interface [COM], IPropertyPageSite interface [COM],described, _ctrl_ipropertypagesite, com.ipropertypagesite, ocidl/IPropertyPageSite
ms.topic: interface
f1_keywords: 
 - "ocidl/IPropertyPageSite"
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
 - IPropertyPageSite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyPageSite interface


## -description


Provides the main features for a property page site object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyPageSite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyPageSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyPageSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getlocaleid">GetLocaleID</a>
</td>
<td align="left" width="63%">
Retrieves the locale identifier (an LCID) that a property page can use to adjust its locale-specific settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getpagecontainer">GetPageContainer</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the object representing the entire property frame dialog box that contains all the pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-onstatuschange">OnStatusChange</a>
</td>
<td align="left" width="63%">
Informs the frame that the property page managed by this site has changed its state, that is, one or more property values have been changed in the page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-translateaccelerator">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Passes a keystroke to the property frame for processing.

</td>
</tr>
</table> 


## -remarks



For each property page created within a property frame, the frame creates a property page site to provide information to the property page and to receive notifications from the page when changes occur. This latter notification is used to initiate a call to <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-ispagedirty">IPropertyPage::IsPageDirty</a>, the return value of which is then used to enable or disable the frame's <b>Apply</b> button.

<h3><a id="OLE_Implementation"></a><a id="ole_implementation"></a><a id="OLE_IMPLEMENTATION"></a>OLE Implementation</h3>
The system provides an implementation of the <b>IPropertyPageSite</b> interface through the <a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframe">OleCreatePropertyFrame</a> or <a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframeindirect">OleCreatePropertyFrameIndirect</a> functions. The frame implementation provided through these functions only implements the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-onstatuschange">OnStatusChange</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getlocaleid">GetLocaleID</a> methods. The <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getpagecontainer">GetPageContainer</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-translateaccelerator">TranslateAccelerator</a> methods return E_NOTIMPL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iperpropertybrowsing">IPerPropertyBrowsing</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ispecifypropertypages">ISpecifyPropertyPage</a>
 

 

