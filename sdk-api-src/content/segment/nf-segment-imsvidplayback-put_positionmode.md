---
UID: NF:segment.IMSVidPlayback.put_PositionMode
title: IMSVidPlayback::put_PositionMode
author: windows-sdk-content
description: The put_PositionMode method specifies how position values will be interpreted by this interface.
old-location: mstv\imsvidplayback_put_positionmode.htm
tech.root: MSTV
ms.assetid: b2ff0b7e-c35d-4ea9-92de-a31654781687
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],put_PositionMode method, IMSVidPlayback.put_PositionMode, IMSVidPlayback::put_PositionMode, IMSVidPlaybackput_PositionMode, mstv.imsvidplayback_put_positionmode, put_PositionMode, put_PositionMode method [Microsoft TV Technologies], put_PositionMode method [Microsoft TV Technologies],IMSVidPlayback interface, segment/IMSVidPlayback::put_PositionMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMSVidPlayback.put_PositionMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidPlayback::put_PositionMode


## -description


The <b>put_PositionMode</b> method specifies how position values will be interpreted by this interface.


## -parameters




### -param lPositionMode [in]

Specifies one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>FrameMode</td>
<td>Position values are specified as frame numbers.</td>
</tr>
<tr>
<td>TenthsSecondsMode</td>
<td>Position values are specified as hundredths of seconds.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The graph is not built. Call the <a href="https://msdn.microsoft.com/49f78dd8-f26e-456d-b67e-155ae0ed5419">Build</a> or <a href="https://msdn.microsoft.com/ec0e2a88-13c0-42f3-ba7d-8ebff1234b86">View</a> method on the Video Control.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed. Possibly the source does not support this mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The value ERROR_INVALID_STATE is converted to an <b>HRESULT</b> with the <b>HRESULT_FROM_WIN32</b> macro.</div>
<div> </div>



## -remarks



The position mode determines how the parameters are interpreted for the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/a559c0b4-ed63-47ef-b99a-866c87939d5b">IMSVidPlayback::get_Length</a>
</li>
<li>
<a href="https://msdn.microsoft.com/08facda5-3c17-4dac-b06f-6032f9490087">IMSVidPlayback::get_CurrentPosition</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3e9e0128-5609-4a9f-bbfc-a29a2174c5d0">IMSVidPlayback::put_CurrentPosition</a>
</li>
</ul>
Call the <a href="https://msdn.microsoft.com/49f78dd8-f26e-456d-b67e-155ae0ed5419">IMSVidCtl::Build</a> or <a href="https://msdn.microsoft.com/ec0e2a88-13c0-42f3-ba7d-8ebff1234b86">IMSVidCtl::View</a> method before calling this method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
hr = m_pPlayback-&gt;put_PositionMode(TenthsSecondsMode);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ed954545-f58f-4841-9ffd-185350f76388">IMSVidPlayback Interface</a>



<a href="https://msdn.microsoft.com/8a27508c-485c-4371-a997-05fdfb77d17b">get_PositionMode</a>
 

 

