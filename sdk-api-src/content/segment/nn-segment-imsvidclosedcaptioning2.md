---
UID: NN:segment.IMSVidClosedCaptioning2
title: IMSVidClosedCaptioning2
author: windows-sdk-content
description: The IMSVidClosedCaptioning2 interface sets the closed captioning service, such as CC1 or CC2. The MSVidClosedCaptioning feature exposes this interface.
old-location: mstv\imsvidclosedcaptioning2.htm
tech.root: mstv
ms.assetid: 37fe213a-7778-4448-937d-30ad1015d56c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidClosedCaptioning2, IMSVidClosedCaptioning2 interface [Microsoft TV Technologies], IMSVidClosedCaptioning2 interface [Microsoft TV Technologies],described, IMSVidClosedCaptioning2Interface, mstv.imsvidclosedcaptioning2, segment/IMSVidClosedCaptioning2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidClosedCaptioning2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidClosedCaptioning2 interface


## -description



The <b>IMSVidClosedCaptioning2</b> interface sets the closed captioning service, such as CC1 or CC2. The <a href="https://msdn.microsoft.com/9b56ae46-f1b3-41f0-a002-4444f220f767">MSVidClosedCaptioning</a> feature exposes this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidClosedCaptioning2</b> interface inherits from <a href="https://msdn.microsoft.com/070a208b-cf4c-41e1-9a5f-76cc444285c9">IMSVidClosedCaptioning</a>. <b>IMSVidClosedCaptioning2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidClosedCaptioning2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/165e5c75-3ce1-4b37-b577-5aea4af65019">get_Service</a>
</td>
<td align="left" width="63%">
Retrieves the current closed captioning service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f638a7c3-bd0a-465d-b104-ea0066aec6d6">put_Service</a>
</td>
<td align="left" width="63%">
Sets the closed captioning service.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidClosedCaptioning2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/070a208b-cf4c-41e1-9a5f-76cc444285c9">IMSVidClosedCaptioning</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

