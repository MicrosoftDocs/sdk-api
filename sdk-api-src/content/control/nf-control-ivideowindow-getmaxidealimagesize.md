---
UID: NF:control.IVideoWindow.GetMaxIdealImageSize
title: IVideoWindow::GetMaxIdealImageSize
author: windows-sdk-content
description: The GetMaxIdealImageSize method retrieves the maximum ideal image size for the video image.
old-location: dshow\ivideowindow_getmaxidealimagesize.htm
tech.root: DirectShow
ms.assetid: ee9f6803-c8b8-48e0-9be0-3d61a453014e
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetMaxIdealImageSize, GetMaxIdealImageSize method [DirectShow], GetMaxIdealImageSize method [DirectShow],IVideoWindow interface, IVideoWindow interface [DirectShow],GetMaxIdealImageSize method, IVideoWindow.GetMaxIdealImageSize, IVideoWindow::GetMaxIdealImageSize, IVideoWindowGetMaxIdealImageSize, control/IVideoWindow::GetMaxIdealImageSize, dshow.ivideowindow_getmaxidealimagesize
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
<li>The filter is using an <a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay</a> transport.</li>
<li>UseWhenFullScreen mode is on. (See <a href="https://msdn.microsoft.com/e50f7f06-6534-4373-a2b8-fa315158729d">IDirectDrawVideo::UseWhenFullScreen</a>.)</li>
<li>The video surface has no maximum overlay stretch. (The <b>dwMaxOverlayStretch</b> member of the DDCAPS structure is zero. See <a href="https://msdn.microsoft.com/d63437e3-4e8a-49de-b555-db29d235569d">IDirectDrawVideo::GetCaps</a>.)</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/b2d1d267-008d-402a-864a-e801e7581fbd">IVideoWindow::GetMinIdealImageSize</a>
 

 

