---
UID: NN:segment.IMSVidPlayback
title: IMSVidPlayback
author: windows-driver-content
description: The IMSVidPlayback interface controls a Video Control playback device.
old-location: mstv\imsvidplayback.htm
old-project: mstv
ms.assetid: ed954545-f58f-4841-9ffd-185350f76388
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidPlayback, IMSVidPlayback interface [Microsoft TV Technologies], IMSVidPlayback interface [Microsoft TV Technologies],described, IMSVidPlaybackInterface, mstv.imsvidplayback, segment/IMSVidPlayback
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
-	IMSVidPlayback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidPlayback interface


## -description



The <b>IMSVidPlayback</b> interface controls a Video Control playback device.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidPlayback</b> interface inherits from <a href="https://msdn.microsoft.com/5b413ade-4ab2-45fa-98b2-fd93c8f89a43">IMSVidInputDevice</a>. <b>IMSVidPlayback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidPlayback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41aad247-1f04-4245-89df-8ac527926307">get_CanStep</a>
</td>
<td align="left" width="63%">
Queries whether the input source can step frame by frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08facda5-3c17-4dac-b06f-6032f9490087">get_CurrentPosition</a>
</td>
<td align="left" width="63%">
Returns the current playback position of the source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ea9ad29-9903-41ac-9be8-acb41cec10d1">get_EnableResetOnStop</a>
</td>
<td align="left" width="63%">
Indicates how playback will resume if the graph is rebuilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a559c0b4-ed63-47ef-b99a-866c87939d5b">get_Length</a>
</td>
<td align="left" width="63%">
Retrieves the length of the playback source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a27508c-485c-4371-a997-05fdfb77d17b">get_PositionMode</a>
</td>
<td align="left" width="63%">
Indicates how position values are interpreted by this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f91c728-23c7-4559-9c72-ddd92b0b0212">get_Rate</a>
</td>
<td align="left" width="63%">
Retrieves the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">
Pauses the playback device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e9e0128-5609-4a9f-bbfc-a29a2174c5d0">put_CurrentPosition</a>
</td>
<td align="left" width="63%">
Seeks to a specified position in the source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2b4285c-3cf8-40dc-87eb-57419ef7343e">put_EnableResetOnStop</a>
</td>
<td align="left" width="63%">
Specifies how playback will resume if the graph is rebuilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2ff0b7e-c35d-4ea9-92de-a31654781687">put_PositionMode</a>
</td>
<td align="left" width="63%">
Specifies how position values will be interpreted by this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3542d7c-6333-4832-a24a-0b778ea83a4c">put_Rate</a>
</td>
<td align="left" width="63%">
Sets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a>
</td>
<td align="left" width="63%">
Runs the playback device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e971571-61f4-4b24-81a7-45fa17b6b785">Step</a>
</td>
<td align="left" width="63%">
Steps through the video stream by a specified number of frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops the playback device.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidPlayback)</code>.




## -see-also




<a href="https://msdn.microsoft.com/5b413ade-4ab2-45fa-98b2-fd93c8f89a43">IMSVidInputDevice</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

