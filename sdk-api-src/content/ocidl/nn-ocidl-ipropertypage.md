---
UID: NN:ocidl.IPropertyPage
title: IPropertyPage (ocidl.h)
author: windows-sdk-content
description: Provides the main features of a property page object that manages a particular page within a property sheet.
old-location: com\ipropertypage.htm
tech.root: com
ms.assetid: ad2cb3ae-dd24-4774-95bd-f5a0773c68b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPropertyPage, IPropertyPage interface [COM], IPropertyPage interface [COM],described, _ctrl_ipropertypage, com.ipropertypage, ocidl/IPropertyPage
ms.topic: interface
f1_keywords: ["ocidl/IPropertyPage"]
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
 - IPropertyPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyPage interface


## -description


Provides the main features of a property page object that manages a particular page within a property sheet. A property page implements at least <b>IPropertyPage</b> and can optionally implement <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a> if selection of a specific property is supported. See <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-mappropertytopage">IPerPropertyBrowsing::MapPropertyToPage</a> for more information on specific property browsing. The methods of <b>IPropertyPage2</b> enable the property sheet or property frame to instruct the page when to perform specific actions, mostly based on user input such as switching between pages or pressing various buttons that the frame itself manages in the dialog box.

A property page manages a dialog box that contains only those controls that should be displayed for that one page within the property sheet itself. This means that the dialog box template used to define the page should only carry the WS_CHILD style and no others. It should not include any style related to a frame, caption, or system menus or controls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyPage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyPage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyPage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-activate">Activate</a>
</td>
<td align="left" width="63%">
Creates the dialog box window for the property page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-apply">Apply</a>
</td>
<td align="left" width="63%">
Applies the current values to the underlying objects associated with the property page as previously passed to <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-setobjects">IPropertyPage::SetObjects</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-deactivate">Deactivate</a>
</td>
<td align="left" width="63%">
Destroys the window created in <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-activate">IPropertyPage::Activate</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-getpageinfo">GetPageInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the property page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-help">Help</a>
</td>
<td align="left" width="63%">
Invokes the property page help in response to an end-user request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-ispagedirty">IsPageDirty</a>
</td>
<td align="left" width="63%">
Indicates whether the property page has changed since it was activated or since the most recent call to <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-apply">IPropertyPage::Apply</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-move">Move</a>
</td>
<td align="left" width="63%">
Positions and resizes the property page dialog box within the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-setobjects">SetObjects</a>
</td>
<td align="left" width="63%">
Provides the property page with an array of pointers to objects associated with this property page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-setpagesite">SetPageSite</a>
</td>
<td align="left" width="63%">
Initializes a property page and provides the page with a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a> interface through which the property page communicates with the property frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-show">Show</a>
</td>
<td align="left" width="63%">
Makes the property page dialog box visible or invisible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-translateaccelerator">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Passes a keystroke to the property page for processing.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iperpropertybrowsing">IPerPropertyBrowsing</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ispecifypropertypages">ISpecifyPropertyPage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframe">OleCreatePropertyFrame</a>



<a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframeindirect">OleCreatePropertyFrameIndirect</a>
 

 

