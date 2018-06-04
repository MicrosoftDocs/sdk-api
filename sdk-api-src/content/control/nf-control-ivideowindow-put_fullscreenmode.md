---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IVideoWindow::put_FullScreenMode


## -description



The <code>put_FullScreenMode</code> method enables or disables full-screen video rendering.




## -parameters




### -param FullScreenMode [in]

Boolean value that specifies whether to enable or disable full-screen mode. Must be one of the following values:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>
                  OATRUE
                </td>
<td>Switch to full-screen mode.</td>
</tr>
<tr>
<td>
                  OAFALSE
                </td>
<td>Disable full-screen mode. (Default.)</td>
</tr>
</table>
 


## -returns



Possible return values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Filter does not support full-screen mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Already in the requested mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_FULLSCREEN</b></dt>
</dl>
</td>
<td width="60%">
Could not find any filter that supports full-screen mode.

</td>
</tr>
</table>
 




## -remarks



Depending on the video renderer, the switch to full-screen mode may not be visible until the application runs or pauses the graph. In full-screen mode, if the user switches away from the application (for example, using ALT + TAB), the Filter Graph Manager sends an <a href="https://msdn.microsoft.com/f720a9b6-930a-4ed7-9798-1c72fa7a11ff">EC_FULLSCREEN_LOST</a> event.

The following remarks describe how the Filter Graph Manager implements full-screen mode. Application developers can probably ignore this information, but it may be useful if you are writing a custom video renderer.

When an application switches to full-screen mode, the Filter Graph Manager searches for a video renderer that will function most efficiently. In order of preference, these are:

<ol>
<li>Any video renderer in the filter graph that natively supports full-screen mode.</li>
<li>Any video renderer in the filter graph that can stretch the video to full-screen without a significant performance cost.</li>
<li>The <a href="https://msdn.microsoft.com/59332096-bdfe-4208-b99a-1f434652f287">Full Screen Renderer</a> filter.</li>
<li>Any video renderer in the filter graph that supports <b>IVideoWindow</b>.</li>
</ol>
For the first option, the Filter Graph Manager calls <a href="https://msdn.microsoft.com/742587c7-545a-4c5f-bff1-511ed6d0b1d5">IVideoWindow::get_FullScreenMode</a> on every video renderer in the graph. Most renderers return E_NOTIMPL, indicating the filter does not natively support full-screen mode. If any renderer returns a value not equal to E_NOTIMPL, the Filter Graph Manager uses that one.

For the second option, the Filter Graph Manager calls <a href="https://msdn.microsoft.com/ee9f6803-c8b8-48e0-9be0-3d61a453014e">IVideoWindow::GetMaxIdealImageSize</a> and <b>GetMinIdealImageSize</b> on every video renderer in the graph. If the size of the display falls within the filter's reported range, it indicates that the filter can stretch the video without a significant performance cost.

<div class="alert"><b>Note</b>  If the graph is stopped, the Filter Graph Manager pauses each renderer before calling these methods. This gives the renderer an opportunity to initialize any resources it needs, because many renderers cannot determine these values while they are stopped.</div>
<div> </div>
Except on older hardware, the second option will generally succeed. The third option is to use the Full Screen Renderer filter, adding it to the graph if necessary. The fourth option is simply to find the first renderer in the graph that supports <b>IVideoWindow</b>, and stretch the video regardless of performance.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/742587c7-545a-4c5f-bff1-511ed6d0b1d5">IVideoWindow::get_FullScreenMode</a>
 

 

