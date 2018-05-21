---
UID: NN:segment.IMSVidAudioRenderer
title: IMSVidAudioRenderer
author: windows-driver-content
description: The IMSVidAudioRenderer interface represents an audio renderer device. It enables applications to control the volume and balance. To retrieve the audio renderer device that is currently active, call the IMSVidCtl::get_AudioRendererActive method.
old-location: mstv\imsvidaudiorenderer.htm
old-project: mstv
ms.assetid: f822b5a6-c88e-48c9-91f4-611a3f147fe0
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidAudioRenderer, IMSVidAudioRenderer interface [Microsoft TV Technologies], IMSVidAudioRenderer interface [Microsoft TV Technologies],described, IMSVidAudioRendererInterface, mstv.imsvidaudiorenderer, segment/IMSVidAudioRenderer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidAudioRenderer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidAudioRenderer interface


## -description



The <b>IMSVidAudioRenderer</b> interface represents an audio renderer device. It enables applications to control the volume and balance. To retrieve the audio renderer device that is currently active, call the <a href="https://msdn.microsoft.com/4ac78904-18ca-4bcb-9c0e-15595a756ecd">IMSVidCtl::get_AudioRendererActive</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidAudioRenderer</b> interface inherits from <a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a>. <b>IMSVidAudioRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidAudioRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59def393-ab3d-41a8-968a-cd22429874a0">get_Balance</a>
</td>
<td align="left" width="63%">
Retrieves the balance level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dbbdb17-b077-4e36-a5d4-c8e343feb930">get_Volume</a>
</td>
<td align="left" width="63%">
Retrieves the volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25a9231a-d34a-4657-be0a-fcc979d1745d">put_Balance</a>
</td>
<td align="left" width="63%">
Specifies the balance level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0fa96bb-a903-41e1-bd2a-6ef1733adbd4">put_Volume</a>
</td>
<td align="left" width="63%">
Specifies the volume level.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAudioRenderer)</code>.




## -see-also




<a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

