---
UID: NF:control.IVideoWindow.GetMinIdealImageSize
title: IVideoWindow::GetMinIdealImageSize
author: windows-sdk-content
description: The GetMinIdealImageSize method retrieves the minimum ideal size for the video image.
old-location: dshow\ivideowindow_getminidealimagesize.htm
tech.root: DirectShow
ms.assetid: b2d1d267-008d-402a-864a-e801e7581fbd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetMinIdealImageSize, GetMinIdealImageSize method [DirectShow], GetMinIdealImageSize method [DirectShow],IVideoWindow interface, IVideoWindow interface [DirectShow],GetMinIdealImageSize method, IVideoWindow.GetMinIdealImageSize, IVideoWindow::GetMinIdealImageSize, IVideoWindowGetMinIdealImageSize, control/IVideoWindow::GetMinIdealImageSize, dshow.ivideowindow_getminidealimagesize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVideoWindow.GetMinIdealImageSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::GetMinIdealImageSize


## -description



The <code>GetMinIdealImageSize</code> method retrieves the minimum ideal size for the video image.




## -parameters




### -param pWidth [out]

Receives the minimum ideal width, in pixels.
          


### -param pHeight [out]

Receives the minimum ideal height, in pixels.
          


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Could not retrieve a minimum image size.

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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Filter is stopped.

</td>
</tr>
</table>
 




## -remarks



The maximum ideal size may differ from the native video size, because the video hardware might have specific stretching requirements.

This method returns S_FALSE under various circumstances:

<ul>
<li>The filter is using an <a href="https://msdn.microsoft.com/en-us/library/Dd390357(v=VS.85).aspx">IOverlay</a> transport.</li>
<li>UseWhenFullScreen mode is on. (See <a href="https://msdn.microsoft.com/en-us/library/Dd406831(v=VS.85).aspx">IDirectDrawVideo::UseWhenFullScreen</a>.)</li>
<li>Video playback is using a stretchable offscreen surface. (The <b>dwCaps</b> member of the DDCAPS structure includes the DDCAPS_BLTSTRETCH flag. See <a href="https://msdn.microsoft.com/en-us/library/Dd406819(v=VS.85).aspx">IDirectDrawVideo::GetCaps</a>.)</li>
<li>The video surface has no minimum overlay stretch. (The <b>dwMinOverlayStretch</b> member of the DDCAPS structure is zero. See <a href="https://msdn.microsoft.com/en-us/library/Dd406819(v=VS.85).aspx">IDirectDrawVideo::GetCaps</a>.)</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377282(v=VS.85).aspx">IVideoWindow::GetMaxIdealImageSize</a>
 

 

