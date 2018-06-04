---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMSVidGraphSegmentContainer interface


## -description



The <b>IMSVidGraphSegmentContainer</b> interface is exposed by the Video Control and contains one supported method, <a href="https://msdn.microsoft.com/fecc2953-84d6-4d1b-bb3f-5b966debef1e">get_Graph</a>, which obtains a pointer to the Filter Graph Manager. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidGraphSegmentContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMSVidGraphSegmentContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidGraphSegmentContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fecc2953-84d6-4d1b-bb3f-5b966debef1e">get_Graph</a>
</td>
<td align="left" width="63%">
Returns a pointer to the Filter Graph Manager.

</td>
</tr>
</table> 


## -remarks



This interface has additional methods besides the one shown here, but they are not supported.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidGraphSegmentContainer)</code>.




## -see-also




<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

