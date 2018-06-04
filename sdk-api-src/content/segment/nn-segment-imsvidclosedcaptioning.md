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

# IMSVidClosedCaptioning interface


## -description



The <b>IMSVidClosedCaptioning</b> interface enables or disables closed captions. The <a href="https://msdn.microsoft.com/9b56ae46-f1b3-41f0-a002-4444f220f767">MSVidClosedCaptioning</a> feature exposes this interface.

To obtain this interface, enumerate the collection of available features on the Video Control. To use closed captioning, activate the closed captioning feature before you build the graph. Once the feature is active, you can enable or disable the closed captioning display by calling the <a href="https://msdn.microsoft.com/2485b634-24e9-4945-ae46-0ca7fdb9d92b">IMSVidClosedCaptioning::put_Enable</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidClosedCaptioning</b> interface inherits from <a href="https://msdn.microsoft.com/0512e1d6-e10e-421e-846c-4bcd7e86d0e7">IMSVidFeature</a>. <b>IMSVidClosedCaptioning</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidClosedCaptioning</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bb46aa7-fd94-4afa-9bba-769472e014ff">get_Enable</a>
</td>
<td align="left" width="63%">
Queries whether closed captioning is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2485b634-24e9-4945-ae46-0ca7fdb9d92b">put_Enable</a>
</td>
<td align="left" width="63%">
Enables or disables closed captioning.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidClosedCaptioning)</code>.




## -see-also




<a href="https://msdn.microsoft.com/699f4021-1c9c-4855-8295-5b84bc512252">Displaying Closed Captioning in C++</a>



<a href="https://msdn.microsoft.com/0512e1d6-e10e-421e-846c-4bcd7e86d0e7">IMSVidFeature</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

