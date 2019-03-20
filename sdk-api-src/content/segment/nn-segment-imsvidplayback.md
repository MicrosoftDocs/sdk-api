---
UID: NN:segment.IMSVidPlayback
title: IMSVidPlayback (segment.h)
author: windows-sdk-content
description: The IMSVidPlayback interface controls a Video Control playback device.
old-location: mstv\imsvidplayback.htm
tech.root: mstv
ms.assetid: ed954545-f58f-4841-9ffd-185350f76388
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidPlayback, IMSVidPlayback interface [Microsoft TV Technologies], IMSVidPlayback interface [Microsoft TV Technologies],described, IMSVidPlaybackInterface, mstv.imsvidplayback, segment/IMSVidPlayback
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
 - IMSVidPlayback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Dd694589(v=VS.85).aspx">get_CanStep</a>
</td>
<td align="left" width="63%">
Queries whether the input source can step frame by frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694590(v=VS.85).aspx">get_CurrentPosition</a>
</td>
<td align="left" width="63%">
Returns the current playback position of the source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694591(v=VS.85).aspx">get_EnableResetOnStop</a>
</td>
<td align="left" width="63%">
Indicates how playback will resume if the graph is rebuilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694592(v=VS.85).aspx">get_Length</a>
</td>
<td align="left" width="63%">
Retrieves the length of the playback source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694593(v=VS.85).aspx">get_PositionMode</a>
</td>
<td align="left" width="63%">
Indicates how position values are interpreted by this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694594(v=VS.85).aspx">get_Rate</a>
</td>
<td align="left" width="63%">
Retrieves the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694595(v=VS.85).aspx">Pause</a>
</td>
<td align="left" width="63%">
Pauses the playback device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694596(v=VS.85).aspx">put_CurrentPosition</a>
</td>
<td align="left" width="63%">
Seeks to a specified position in the source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694597(v=VS.85).aspx">put_EnableResetOnStop</a>
</td>
<td align="left" width="63%">
Specifies how playback will resume if the graph is rebuilt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694598(v=VS.85).aspx">put_PositionMode</a>
</td>
<td align="left" width="63%">
Specifies how position values will be interpreted by this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694599(v=VS.85).aspx">put_Rate</a>
</td>
<td align="left" width="63%">
Sets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694600(v=VS.85).aspx">Run</a>
</td>
<td align="left" width="63%">
Runs the playback device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694601(v=VS.85).aspx">Step</a>
</td>
<td align="left" width="63%">
Steps through the video stream by a specified number of frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694602(v=VS.85).aspx">Stop</a>
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
 

 

