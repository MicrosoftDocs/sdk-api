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

# IVPConfig interface


## -description




          The <b>IVPConfig</b> interface must be implemented by any filter that wraps a hardware decoder with a video port. This enables the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a>, through its <a href="https://msdn.microsoft.com/6b40ba9e-8562-4d31-beaf-e4d4858bf145">IVPNotify</a> interface, to set and retrieve configuration information on the video port regarding the video memory on the display adapter. This interface derives from <a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig</a>.

Applications never use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPConfig</b> interface inherits from <a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig</a>. <b>IVPConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVPConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2362e321-cbdd-41ee-97ff-e6ff9cd672b0">IsVPDecimationAllowed</a>
</td>
<td align="left" width="63%">
Given the context, retrieves whether scaling at the video port is possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62b8281e-6feb-43f5-b1a5-36444fda5543">SetScalingFactors</a>
</td>
<td align="left" width="63%">
Sets the factors by which the decoder should scale the video stream.

</td>
</tr>
</table> 


## -remarks




        Include Dvp.h and Vptype.h before Vpconfig.h.
      




## -see-also




<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig</a>



<a href="https://msdn.microsoft.com/c72bd662-366c-4102-9ad9-9e4c59096ede">IVPBaseNotify</a>



<a href="https://msdn.microsoft.com/8d5fc7ee-93ee-4297-ba24-0eed63bec1ea">IVPNotify2</a>
 

 

