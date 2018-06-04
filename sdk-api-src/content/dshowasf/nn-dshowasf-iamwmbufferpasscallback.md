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

# IAMWMBufferPassCallback interface


## -description



The <code>IAMWMBufferPassCallback</code> interface is a callback interface used with the <a href="https://msdn.microsoft.com/82b9f849-b9dc-439b-8ca7-9dcd992338ab">WM ASF Reader</a> and <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> filters. Applications can use this interface to get or set properties on individual samples, before the samples are passed downstream for further processing.

Applications can use this interface to retrieve data unit extensions such as the SMPTE time code for each sample. Another common use for this interface is to force key-frame insertion in a variable bit rate video stream during file writing.

To use this interface, query the filter's pin for the <a href="https://msdn.microsoft.com/c13fe4e0-0847-4799-92a6-da36375cfbf4">IAMWMBufferPass</a> interface and call <a href="https://msdn.microsoft.com/4aa6fc71-39a7-4fa5-bfe3-b5b12dd44a2b">IAMWMBufferPass::SetNotify</a> with a pointer to your implementation of the callback interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMWMBufferPassCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMWMBufferPassCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMWMBufferPassCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13778b61-0e75-412f-b1e4-eaaf5ec0c853">Notify</a>
</td>
<td align="left" width="63%">
Called by the filter for each buffer that is delivered during streaming.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c13fe4e0-0847-4799-92a6-da36375cfbf4">IAMWMBufferPass Interface</a>



<a href="https://msdn.microsoft.com/2fae0504-d1da-413a-80dd-de7818f506ef">Using Windows Media in DirectShow</a>
 

 

