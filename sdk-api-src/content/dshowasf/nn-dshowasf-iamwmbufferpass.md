---
UID: NN:dshowasf.IAMWMBufferPass
title: IAMWMBufferPass
author: windows-sdk-content
description: The IAMWMBufferPass interface is implemented on the output pins of the WM ASF Reader and the input pins of the WM ASF Writer.
old-location: dshow\iamwmbufferpass.htm
old-project: DirectShow
ms.assetid: c13fe4e0-0847-4799-92a6-da36375cfbf4
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMWMBufferPass, IAMWMBufferPass interface [DirectShow], IAMWMBufferPass interface [DirectShow],described, IAMWMBufferPassInterface, dshow.iamwmbufferpass, dshowasf/IAMWMBufferPass
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IAMWMBufferPass
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAMWMBufferPass interface


## -description



The <code>IAMWMBufferPass</code> interface is implemented on the output pins of the <a href="https://msdn.microsoft.com/82b9f849-b9dc-439b-8ca7-9dcd992338ab">WM ASF Reader</a> and the input pins of the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a>. Applications can use this interface to get or set properties on individual samples in an ASF stream. Applications can also use it to get or set data unit extensions. To use this interface, implement the <a href="https://msdn.microsoft.com/c3a8e01e-a626-4e47-ad98-e22d1fe88906">IAMWMBufferPassCallback</a> interface in your application. Then call <a href="https://msdn.microsoft.com/4aa6fc71-39a7-4fa5-bfe3-b5b12dd44a2b">IAMWMBufferPass::SetNotify</a> on the filter's pin with a pointer to the callback interface.

One common use for this interface is to force key-frame insertion in a variable bit rate video stream during file writing. To do this, you must set the <b>WM_SampleExtensionGUID_OutputCleanPoint</b> property using the <a href="https://msdn.microsoft.com/3ebf80d0-b5b0-4024-805d-e0a3855574bf">INSSBuffer3</a> interface on the sample. For more information about sample extensions, see the Windows Media Format SDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMWMBufferPass</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMWMBufferPass</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMWMBufferPass</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4aa6fc71-39a7-4fa5-bfe3-b5b12dd44a2b">SetNotify</a>
</td>
<td align="left" width="63%">
Sets an application-defined callback on the filter.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2fae0504-d1da-413a-80dd-de7818f506ef">Using Windows Media in DirectShow</a>
 

 

