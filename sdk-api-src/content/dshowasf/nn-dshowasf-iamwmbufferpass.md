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
f1_keywords: 
 - "dshowasf/IAMWMBufferPass"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMWMBufferPass interface


## -description



The <b>IAMWMBufferPass</b> interface is implemented on the output pins of the <a href="https://docs.microsoft.com/windows/desktop/wmformat/wm-asf-reader-filter">WM ASF Reader</a> and the input pins of the <a href="https://docs.microsoft.com/windows/desktop/wmformat/wm-asf-writer-filter">WM ASF Writer</a>. Applications use it to give the pin a pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd798277(v=vs.85)">IAMWMBufferPassCallback</a> interface on an application-defined object that gets and sets properties and data unit extensions on individual samples in a stream. One common use for this interface is to force key-frame insertion in a variable bit rate video stream during file writing. To do this, you must set the <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">cleanpoint</a> property on individual <b>INSSBuffer3</b> samples.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMWMBufferPass</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMWMBufferPass</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/wmformat/iamwmbufferpass-setnotify">SetNotify</a>
</td>
<td align="left" width="63%">
Used by applications to provide the WM ASF Writer or <a href="https://docs.microsoft.com/windows/desktop/wmformat/wm-asf-reader-filter">WM ASF Reader</a> filter with a pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd798277(v=vs.85)">IAMWMBufferPassCallback</a> interface on an application-defined object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/directshow-qasf-reference">DirectShow QASF Reference</a>
 

 

