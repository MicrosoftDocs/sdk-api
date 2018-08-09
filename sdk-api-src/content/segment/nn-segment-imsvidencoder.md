---
UID: NN:segment.IMSVidEncoder
title: IMSVidEncoder
author: windows-sdk-content
description: The IMSVidEncoder interface represents the MSVidEncoder feature object, which is required for stream buffer applications using the Video Control. For more information, see Using the Stream Buffer Engine with the Video Control.
old-location: mstv\imsvidencoder.htm
old-project: mstv
ms.assetid: 37d03dff-ae40-4e7f-a66f-facd0c1f6eee
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidEncoder, IMSVidEncoder interface [Microsoft TV Technologies], IMSVidEncoder interface [Microsoft TV Technologies],described, IMSVidEncoderInterface, mstv.imsvidencoder, segment/IMSVidEncoder
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidEncoder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidEncoder interface


## -description



The <b>IMSVidEncoder</b> interface represents the <a href="https://msdn.microsoft.com/f6cc4c5b-84ae-4b3f-b68d-b37c3826251f">MSVidEncoder</a> feature object, which is required for stream buffer applications using the Video Control. For more information, see <a href="https://msdn.microsoft.com/41b458d6-e2c1-4587-9342-91aa13f91b86">Using the Stream Buffer Engine with the Video Control</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidEncoder</b> interface inherits from <a href="https://msdn.microsoft.com/0512e1d6-e10e-421e-846c-4bcd7e86d0e7">IMSVidFeature</a>. <b>IMSVidEncoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidEncoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b22a062-7da5-411e-ac85-fb9c7b3650a7">get_AudioEncoderInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the audio encoder interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6ee3169-ba24-495f-b446-161c899aab16">get_VideoEncoderInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the video encoder interface.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidEncoder)</code>.




## -see-also




<a href="https://msdn.microsoft.com/0512e1d6-e10e-421e-846c-4bcd7e86d0e7">IMSVidFeature</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

