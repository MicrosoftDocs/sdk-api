---
UID: NF:control.IVideoWindow.GetMaxIdealImageSize
title: IVideoWindow::GetMaxIdealImageSize (control.h)
author: windows-sdk-content
description: The GetMaxIdealImageSize method retrieves the maximum ideal image size for the video image.
old-location: dshow\ivideowindow_getmaxidealimagesize.htm
tech.root: DirectShow
ms.assetid: ee9f6803-c8b8-48e0-9be0-3d61a453014e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMaxIdealImageSize, GetMaxIdealImageSize method [DirectShow], GetMaxIdealImageSize method [DirectShow],IVideoWindow interface, IVideoWindow interface [DirectShow],GetMaxIdealImageSize method, IVideoWindow.GetMaxIdealImageSize, IVideoWindow::GetMaxIdealImageSize, IVideoWindowGetMaxIdealImageSize, control/IVideoWindow::GetMaxIdealImageSize, dshow.ivideowindow_getmaxidealimagesize
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
 - IVideoWindow.GetMaxIdealImageSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::GetMaxIdealImageSize


## -description



The <code>GetMaxIdealImageSize</code> method retrieves the maximum ideal image size for the video image.




## -parameters




### -param pWidth [out]

Receives the maximum ideal width, in pixels.
          


### -param pHeight [out]

Receives the maximum ideal height, in pixels.
          


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
Could not retrieve a maximum image size.

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
<li>The video surface has no maximum overlay stretch. (The <b>dwMaxOverlayStretch</b> member of the DDCAPS structure is zero. See <a href="https://msdn.microsoft.com/en-us/library/Dd406819(v=VS.85).aspx">IDirectDrawVideo::GetCaps</a>.)</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377284(v=VS.85).aspx">IVideoWindow::GetMinIdealImageSize</a>
 

 

