---
UID: NN:ocidl.IPropertyPage2
title: IPropertyPage2
author: windows-sdk-content
description: An extension to IPropertyPage to support initial selection of a property on a page.
old-location: com\ipropertypage2.htm
tech.root: com
ms.assetid: 65cd8f97-f88c-433c-b4e7-9dace7193ec1
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IPropertyPage2, IPropertyPage2 interface [COM], IPropertyPage2 interface [COM],described, _ctrl_ipropertypage2, com.ipropertypage2, ocidl/IPropertyPage2
ms.prod: windows
ms.technology: windows-sdk
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
 - IPropertyPage2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyPage2 interface


## -description


An extension to <a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a> to support initial selection of a property on a page.

This method works in conjunction with the implementation of <a href="https://msdn.microsoft.com/f8cf86eb-23d1-4aa6-859a-055df99b064c">IPerPropertyBrowsing::MapPropertyToPage</a> on an object that supplies properties and specifies property pages through <a href="https://msdn.microsoft.com/fd986241-aabe-477e-a382-28a1ecfd5410">ISpecifyPropertyPages</a>. This interface has only one extra method in addition to those in <a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>. That method, <a href="https://msdn.microsoft.com/a41d2d50-6484-43d0-a41c-1cfa3bfdbe8e">IPropertyPage2::EditProperty</a> tells the page which property to highlight.


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
<a href="https://msdn.microsoft.com/a41d2d50-6484-43d0-a41c-1cfa3bfdbe8e">EditProperty</a>
</td>
<td align="left" width="63%">
Specifies which field is to receive the focus when the property page is activated.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/05e46df3-b6c8-4520-af11-21e1ff90fb9f">IPerPropertyBrowsing</a>



<a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>



<a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a>



<a href="https://msdn.microsoft.com/fd986241-aabe-477e-a382-28a1ecfd5410">ISpecifyPropertyPage</a>
 

 

