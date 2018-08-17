---
UID: NN:ocidl.IPropertyPageSite
title: IPropertyPageSite
author: windows-sdk-content
description: Provides the main features for a property page site object.
old-location: com\ipropertypagesite.htm
old-project: com
ms.assetid: a9035a10-2078-4626-8386-f9298526dfb7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPropertyPageSite, IPropertyPageSite interface [COM], IPropertyPageSite interface [COM],described, _ctrl_ipropertypagesite, com.ipropertypagesite, ocidl/IPropertyPageSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ocidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPropertyPageSite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyPageSite interface


## -description


Provides the main features for a property page site object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyPageSite</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IPropertyPageSite</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d569346d-4a40-42a4-ac8e-539588c4dd66">GetLocaleID</a>
</td>
<td align="left" width="63%">
Retrieves the locale identifier (an LCID) that a property page can use to adjust its locale-specific settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88cbefe6-51c7-4c09-80bb-677c83f97cac">GetPageContainer</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the object representing the entire property frame dialog box that contains all the pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cea36260-b0f6-489a-b02a-3ca3576c6431">OnStatusChange</a>
</td>
<td align="left" width="63%">
Informs the frame that the property page managed by this site has changed its state, that is, one or more property values have been changed in the page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2233022-e66e-448c-a921-92948c05016f">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Passes a keystroke to the property frame for processing.

</td>
</tr>
</table> 


## -remarks



For each property page created within a property frame, the frame creates a property page site to provide information to the property page and to receive notifications from the page when changes occur. This latter notification is used to initiate a call to <a href="https://msdn.microsoft.com/6a19a659-8fab-4218-bc5a-c53860f578f6">IPropertyPage::IsPageDirty</a>, the return value of which is then used to enable or disable the frame's <b>Apply</b> button.

<h3><a id="OLE_Implementation"></a><a id="ole_implementation"></a><a id="OLE_IMPLEMENTATION"></a>OLE Implementation</h3>
The system provides an implementation of the <b>IPropertyPageSite</b> interface through the <a href="https://msdn.microsoft.com/06f75ac2-3ee6-4209-83cf-a4e5244a18bd">OleCreatePropertyFrame</a> or <a href="https://msdn.microsoft.com/ccd01d38-2d8e-4509-b44f-fef6ff718558">OleCreatePropertyFrameIndirect</a> functions. The frame implementation provided through these functions only implements the <a href="https://msdn.microsoft.com/cea36260-b0f6-489a-b02a-3ca3576c6431">OnStatusChange</a> and <a href="https://msdn.microsoft.com/d569346d-4a40-42a4-ac8e-539588c4dd66">GetLocaleID</a> methods. The <a href="https://msdn.microsoft.com/88cbefe6-51c7-4c09-80bb-677c83f97cac">GetPageContainer</a> and <a href="https://msdn.microsoft.com/d2233022-e66e-448c-a921-92948c05016f">TranslateAccelerator</a> methods return E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/05e46df3-b6c8-4520-af11-21e1ff90fb9f">IPerPropertyBrowsing</a>



<a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>



<a href="https://msdn.microsoft.com/65cd8f97-f88c-433c-b4e7-9dace7193ec1">IPropertyPage2</a>



<a href="https://msdn.microsoft.com/fd986241-aabe-477e-a382-28a1ecfd5410">ISpecifyPropertyPage</a>
 

 

