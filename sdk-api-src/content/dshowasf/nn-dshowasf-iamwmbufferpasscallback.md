---
UID: NN:dshowasf.IAMWMBufferPassCallback
title: IAMWMBufferPassCallback
author: windows-sdk-content
description: The IAMWMBufferPassCallback interface is provided for advanced scenarios in which applications need access to an INSSBuffer3 sample before it is passed downstream for further processing.
old-location: wmformat\iamwmbufferpasscallback.htm
tech.root: wmformat
ms.assetid: 5bf0ae2e-504b-471b-bfc9-aa48f534e03f
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAMWMBufferPassCallback, IAMWMBufferPassCallback interface [windows Media Format], IAMWMBufferPassCallback interface [windows Media Format],described, IAMWMBufferPassCallbackInterface, dshowasf/IAMWMBufferPassCallback, wmformat.iamwmbufferpasscallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Requires Dshowasf.h, Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IAMWMBufferPassCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMWMBufferPassCallback interface


## -description



The <b>IAMWMBufferPassCallback</b> interface is provided for advanced scenarios in which applications need access to an <b>INSSBuffer3</b> sample before it is passed downstream for further processing. Use this technique to set or retrieve data unit extensions such as the SMPTE time code for each sample. One common use for this interface is to force key-frame insertion in a variable bit rate video stream during file writing. To do this, you must set the <a href="wmformat_glossary.htm">cleanpoint</a> property on individual <b>INSSBuffer3</b> samples. This interface is implemented by applications and called by the WM ASF Writer or <a href="https://msdn.microsoft.com/3d5ca88a-86bd-4d84-b4f4-782564ced58d">WM ASF Reader</a> filter each time a new sample is delivered to the filter.




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
<a href="https://msdn.microsoft.com/3f252754-c784-4ffd-bcfc-fab73fa02b9a">Notify</a>
</td>
<td align="left" width="63%">
Called by the filter for each buffer that is delivered during streaming.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/66f483b5-3886-48b4-bc43-7c3517abd20d">DirectShow QASF Reference</a>



<a href="https://msdn.microsoft.com/aa7513d4-9341-4ddf-ac82-54eb0c6eb5f4">IAMWMBufferPass Interface</a>



<a href="https://msdn.microsoft.com/3ebf80d0-b5b0-4024-805d-e0a3855574bf">INSSBuffer3 Interface</a>
 

 

