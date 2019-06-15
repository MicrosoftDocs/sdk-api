---
UID: NN:dshowasf.IAMWMBufferPassCallback
title: IAMWMBufferPassCallback (dshowasf.h)
author: windows-sdk-content
description: The IAMWMBufferPassCallback interface is provided for advanced scenarios in which applications need access to an INSSBuffer3 sample before it is passed downstream for further processing.
old-location: wmformat\iamwmbufferpasscallback.htm
tech.root: wmformat
ms.assetid: 5bf0ae2e-504b-471b-bfc9-aa48f534e03f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMWMBufferPassCallback, IAMWMBufferPassCallback interface [windows Media Format], IAMWMBufferPassCallback interface [windows Media Format],described, IAMWMBufferPassCallbackInterface, dshowasf/IAMWMBufferPassCallback, wmformat.iamwmbufferpasscallback
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
ms.custom: 19H1
---

# IAMWMBufferPassCallback interface


## -description



The <b>IAMWMBufferPassCallback</b> interface is provided for advanced scenarios in which applications need access to an <b>INSSBuffer3</b> sample before it is passed downstream for further processing. Use this technique to set or retrieve data unit extensions such as the SMPTE time code for each sample. One common use for this interface is to force key-frame insertion in a variable bit rate video stream during file writing. To do this, you must set the <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">cleanpoint</a> property on individual <b>INSSBuffer3</b> samples. This interface is implemented by applications and called by the WM ASF Writer or <a href="https://docs.microsoft.com/windows/desktop/wmformat/wm-asf-reader-filter">WM ASF Reader</a> filter each time a new sample is delivered to the filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMWMBufferPassCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMWMBufferPassCallback</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/wmformat/iamwmbufferpasscallback-notify">Notify</a>
</td>
<td align="left" width="63%">
Called by the filter for each buffer that is delivered during streaming.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/directshow-qasf-reference">DirectShow QASF Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd798276(v=vs.85)">IAMWMBufferPass Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3 Interface</a>
 

 

