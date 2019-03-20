---
UID: NN:segment.IMSVidAudioRendererEvent2
title: IMSVidAudioRendererEvent2 (segment.h)
author: windows-sdk-content
description: Implements an event system for the audio renderer associated with a Video Control.
old-location: mstv\imsvidaudiorendererevent2.htm
tech.root: mstv
ms.assetid: f37d3abb-e8ad-4aae-884a-1c6c4fa445e2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidAudioRendererEvent2, IMSVidAudioRendererEvent2 interface [Microsoft TV Technologies], IMSVidAudioRendererEvent2 interface [Microsoft TV Technologies],described, mstv.imsvidaudiorendererevent2, segment/IMSVidAudioRendererEvent2
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IMSVidAudioRendererEvent2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidAudioRendererEvent2 interface


## -description


Implements an event system for the audio renderer associated with a Video Control. Audio renderer events are triggered by events from the audio decoder upstream of the audio renderer in the filter graph. 

The audio renderer subscribes to audio decoder events by using the <a href="https://msdn.microsoft.com/en-us/library/Dd311961(v=VS.85).aspx">ICodecAPI::RegisterForEvent</a> method. Each method in <b>IMSVidAudioRendererEvent2</b> corresponds to a codec property, as follows:
<ol>
<li>An audio decoder property changes.</li>
<li>The decoder fires an <a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI</a> event. The event data includes the GUID that identifies the codec property.</li>
<li>The audio renderer fires the corresponding <b>IMSVidAudioRendererEvent2</b> event.</li>
</ol>For a list of codec properties, see <a href="https://msdn.microsoft.com/5d527af7-07cf-42e2-99bb-d56c856cc1bc">Codec API Properties</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidAudioRendererEvent2</b> interface inherits from <a href="https://msdn.microsoft.com/50b43d78-7df0-4b23-86c5-76655e22425f">IMSVidAudioRendererEvent</a>. <b>IMSVidAudioRendererEvent2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidAudioRendererEvent2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694454(v=VS.85).aspx">AVAudioChannelConfig</a>
</td>
<td align="left" width="63%">
Indicates a change in the <a href="https://msdn.microsoft.com/ec13bb55-47af-4d79-9560-d297bce8e236">AVAudioChannelConfig</a> property.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694455(v=VS.85).aspx">AVAudioChannelCount</a>
</td>
<td align="left" width="63%">
Indicates a change in the <a href="https://msdn.microsoft.com/e395ce9c-3f11-41e9-8c8c-48c17b217ebc">AVAudioChannelCount</a> property.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694456(v=VS.85).aspx">AVAudioSampleRate</a>
</td>
<td align="left" width="63%">
Indicates a change in the <a href="https://msdn.microsoft.com/9819d6bb-751b-4b47-aa2d-23d7f86c1d3d">AVAudioSampleRate</a> property.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694457(v=VS.85).aspx">AVDDSurroundMode</a>
</td>
<td align="left" width="63%">
Indicates a change in the <a href="https://msdn.microsoft.com/b33839c8-4829-4d90-94de-e461772d3e94">AVDDSurroundMode</a> property.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694458(v=VS.85).aspx">AVDecAudioDualMono</a>
</td>
<td align="left" width="63%">
Indicates a change in the <a href="https://msdn.microsoft.com/96cb9e17-588c-4a1a-a7ba-7f8439d5b79a">AVDecAudioDualMono</a> property.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694459(v=VS.85).aspx">AVDecCommonInputFormat</a>
</td>
<td align="left" width="63%">
Indicates a change in the <a href="https://msdn.microsoft.com/8fddf8c3-268e-4706-9003-e4bfb03d5278">AVDecCommonInputFormat</a> property.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694460(v=VS.85).aspx">AVDecCommonMeanBitRate</a>
</td>
<td align="left" width="63%">
Indicates a change in the <a href="https://msdn.microsoft.com/en-us/library/Dd742710(v=VS.85).aspx">AVDecCommonMeanBitRate</a> property.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694461(v=VS.85).aspx">AVDecCommonOutputFormat</a>
</td>
<td align="left" width="63%">
Indicates a change in the <a href="https://msdn.microsoft.com/fdccdbfa-2814-4d21-9a7f-4121b79718e6">AVDecCommonOutput</a> property.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAudioRendererEvent2)</code>.



