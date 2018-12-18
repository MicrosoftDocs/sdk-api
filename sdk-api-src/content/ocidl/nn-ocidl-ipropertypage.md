---
UID: NN:ocidl.IPropertyPage
title: IPropertyPage
author: windows-sdk-content
description: Provides the main features of a property page object that manages a particular page within a property sheet.
old-location: com\ipropertypage.htm
tech.root: com
ms.assetid: ad2cb3ae-dd24-4774-95bd-f5a0773c68b1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPropertyPage, IPropertyPage interface [COM], IPropertyPage interface [COM],described, _ctrl_ipropertypage, com.ipropertypage, ocidl/IPropertyPage
ms.topic: interface
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
---

# IPropertyPage interface


## -description


Provides the main features of a property page object that manages a particular page within a property sheet. A property page implements at least <b>IPropertyPage</b> and can optionally implement <a href="https://msdn.microsoft.com/65cd8f97-f88c-433c-b4e7-9dace7193ec1">IPropertyPage2</a> if selection of a specific property is supported. See <a href="https://msdn.microsoft.com/f8cf86eb-23d1-4aa6-859a-055df99b064c">IPerPropertyBrowsing::MapPropertyToPage</a> for more information on specific property browsing. The methods of <b>IPropertyPage2</b> enable the property sheet or property frame to instruct the page when to perform specific actions, mostly based on user input such as switching between pages or pressing various buttons that the frame itself manages in the dialog box.

A property page manages a dialog box that contains only those controls that should be displayed for that one page within the property sheet itself. This means that the dialog box template used to define the page should only carry the WS_CHILD style and no others. It should not include any style related to a frame, caption, or system menus or controls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyPage</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IPropertyPage</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4756d06d-0ffc-4214-9c2b-d9cb169b4337">Activate</a>
</td>
<td align="left" width="63%">
Creates the dialog box window for the property page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af0a1b49-54c3-453f-bd6a-70b63d625acb">Apply</a>
</td>
<td align="left" width="63%">
Applies the current values to the underlying objects associated with the property page as previously passed to <a href="https://msdn.microsoft.com/0d7a73ce-8e3c-40c5-9040-6370df5edc2b">IPropertyPage::SetObjects</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/545f7c3d-3c6f-42c2-b472-3da3bc184200">Deactivate</a>
</td>
<td align="left" width="63%">
Destroys the window created in <a href="https://msdn.microsoft.com/4756d06d-0ffc-4214-9c2b-d9cb169b4337">IPropertyPage::Activate</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cb7168c-bb05-4e01-a73b-11a52c5e690b">GetPageInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the property page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba715518-1aa0-42de-bad7-f2d0d0f00460">Help</a>
</td>
<td align="left" width="63%">
Invokes the property page help in response to an end-user request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a19a659-8fab-4218-bc5a-c53860f578f6">IsPageDirty</a>
</td>
<td align="left" width="63%">
Indicates whether the property page has changed since it was activated or since the most recent call to <a href="https://msdn.microsoft.com/af0a1b49-54c3-453f-bd6a-70b63d625acb">IPropertyPage::Apply</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/305857c2-cb3a-4a56-9db3-b986b278bd02">Move</a>
</td>
<td align="left" width="63%">
Positions and resizes the property page dialog box within the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d7a73ce-8e3c-40c5-9040-6370df5edc2b">SetObjects</a>
</td>
<td align="left" width="63%">
Provides the property page with an array of pointers to objects associated with this property page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a57f3f0c-53c0-4ddf-9827-df912f263a9e">SetPageSite</a>
</td>
<td align="left" width="63%">
Initializes a property page and provides the page with a pointer to the <a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a> interface through which the property page communicates with the property frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f89aa820-a3d3-4a41-b2b2-9ee48354fbeb">Show</a>
</td>
<td align="left" width="63%">
Makes the property page dialog box visible or invisible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70501c3d-257c-4981-b841-4bd45f0bec27">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Passes a keystroke to the property page for processing.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/05e46df3-b6c8-4520-af11-21e1ff90fb9f">IPerPropertyBrowsing</a>



<a href="https://msdn.microsoft.com/65cd8f97-f88c-433c-b4e7-9dace7193ec1">IPropertyPage2</a>



<a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a>



<a href="https://msdn.microsoft.com/fd986241-aabe-477e-a382-28a1ecfd5410">ISpecifyPropertyPage</a>



<a href="https://msdn.microsoft.com/06f75ac2-3ee6-4209-83cf-a4e5244a18bd">OleCreatePropertyFrame</a>



<a href="https://msdn.microsoft.com/ccd01d38-2d8e-4509-b44f-fef6ff718558">OleCreatePropertyFrameIndirect</a>
 

 

