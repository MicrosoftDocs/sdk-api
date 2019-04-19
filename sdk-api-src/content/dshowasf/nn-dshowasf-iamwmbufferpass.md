---
UID: NN:dshowasf.IAMWMBufferPass
title: IAMWMBufferPass (dshowasf.h)
author: windows-sdk-content
description: The IAMWMBufferPass interface is implemented on the output pins of the WM ASF Reader and the input pins of the WM ASF Writer.
old-location: wmformat\iamwmbufferpass.htm
tech.root: wmformat
ms.assetid: aa7513d4-9341-4ddf-ac82-54eb0c6eb5f4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMWMBufferPass, IAMWMBufferPass interface [windows Media Format], IAMWMBufferPass interface [windows Media Format],described, IAMWMBufferPassInterface, dshowasf/IAMWMBufferPass, wmformat.iamwmbufferpass
ms.topic: interface
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Requires Dshowasf.h, Windows Media Format 9 Series SDK, or later.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dshowasf.h
api_name:
 - IAMWMBufferPass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMWMBufferPass interface


## -description



The <b>IAMWMBufferPass</b> interface is implemented on the output pins of the <a href="https://msdn.microsoft.com/3d5ca88a-86bd-4d84-b4f4-782564ced58d">WM ASF Reader</a> and the input pins of the <a href="https://msdn.microsoft.com/a902c92e-836d-492c-b2d2-89c216125774">WM ASF Writer</a>. Applications use it to give the pin a pointer to the <a href="https://msdn.microsoft.com/5bf0ae2e-504b-471b-bfc9-aa48f534e03f">IAMWMBufferPassCallback</a> interface on an application-defined object that gets and sets properties and data unit extensions on individual samples in a stream. One common use for this interface is to force key-frame insertion in a variable bit rate video stream during file writing. To do this, you must set the <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">cleanpoint</a> property on individual <b>INSSBuffer3</b> samples.




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
<a href="https://msdn.microsoft.com/b0fff344-a20c-4cfc-828b-c6fc49d990ea">SetNotify</a>
</td>
<td align="left" width="63%">
Used by applications to provide the WM ASF Writer or <a href="https://msdn.microsoft.com/3d5ca88a-86bd-4d84-b4f4-782564ced58d">WM ASF Reader</a> filter with a pointer to the <a href="https://msdn.microsoft.com/5bf0ae2e-504b-471b-bfc9-aa48f534e03f">IAMWMBufferPassCallback</a> interface on an application-defined object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/66f483b5-3886-48b4-bc43-7c3517abd20d">DirectShow QASF Reference</a>
 

 

