---
UID: NF:segment.IMSVidPlayback.get_PositionMode
title: IMSVidPlayback::get_PositionMode (segment.h)
author: windows-sdk-content
description: The get_PositionMode method indicates how position values are interpreted by this interface.
old-location: mstv\imsvidplayback_get_positionmode.htm
tech.root: mstv
ms.assetid: 8a27508c-485c-4371-a997-05fdfb77d17b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],get_PositionMode method, IMSVidPlayback.get_PositionMode, IMSVidPlayback::get_PositionMode, IMSVidPlaybackget_PositionMode, get_PositionMode, get_PositionMode method [Microsoft TV Technologies], get_PositionMode method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_get_positionmode, segment/IMSVidPlayback::get_PositionMode
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
 - IMSVidPlayback.get_PositionMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidPlayback::get_PositionMode


## -description


The <b>get_PositionMode</b> method indicates how position values are interpreted by this interface.


## -parameters




### -param lPositionMode [out]

Pointer to a variable that receives one of the following values.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
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



The value returned by this method determines how the parameters are interpreted for the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd694592(v=VS.85).aspx">IMSVidPlayback::get_Length</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd694590(v=VS.85).aspx">IMSVidPlayback::get_CurrentPosition</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd694596(v=VS.85).aspx">IMSVidPlayback::put_CurrentPosition</a>
</li>
</ul>
Call the <a href="https://msdn.microsoft.com/49f78dd8-f26e-456d-b67e-155ae0ed5419">IMSVidCtl::Build</a> or <a href="https://msdn.microsoft.com/ec0e2a88-13c0-42f3-ba7d-8ebff1234b86">IMSVidCtl::View</a> method before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694586(v=VS.85).aspx">IMSVidPlayback Interface</a>
 

 

