---
UID: NN:ocidl.IPerPropertyBrowsing
title: IPerPropertyBrowsing
author: windows-sdk-content
description: Retrieves the information in the property pages offered by an object.
old-location: com\iperpropertybrowsing.htm
old-project: com
ms.assetid: 05e46df3-b6c8-4520-af11-21e1ff90fb9f
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IPerPropertyBrowsing, IPerPropertyBrowsing interface [COM], IPerPropertyBrowsing interface [COM],described, _ctrl_iperpropertybrowsing, com.iperpropertybrowsing, ocidl/IPerPropertyBrowsing
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IPerPropertyBrowsing
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPerPropertyBrowsing interface


## -description


Retrieves the information in the property pages offered by an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPerPropertyBrowsing</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IPerPropertyBrowsing</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/949d7d12-de59-441d-ac0f-e18f050d005d">GetDisplayString</a>
</td>
<td align="left" width="63%">
Retrieves a text string describing the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b20585f-2bcd-475e-abee-80158692ae0f">GetPredefinedStrings</a>
</td>
<td align="left" width="63%">
Retrieves an array description strings for the allowable values that the specified property can accept.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a532ebed-3ed8-4b49-a17f-f542fdbd74ff">GetPredefinedValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified property that is associated with a predefined string name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8cf86eb-23d1-4aa6-859a-055df99b064c">MapPropertyToPage</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of the property page associated with the specified property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>



<a href="https://msdn.microsoft.com/65cd8f97-f88c-433c-b4e7-9dace7193ec1">IPropertyPage2</a>



<a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a>



<a href="https://msdn.microsoft.com/fd986241-aabe-477e-a382-28a1ecfd5410">ISpecifyPropertyPage</a>
 

 

