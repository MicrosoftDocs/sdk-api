---
UID: NF:amvideo.IFullScreenVideoEx.GetModeInfo
title: IFullScreenVideoEx::GetModeInfo (amvideo.h)
author: windows-sdk-content
description: The GetModeInfo method retrieves information about a specified display mode supported by the Full Screen Renderer filter.
old-location: dshow\ifullscreenvideoex_getmodeinfo.htm
tech.root: DirectShow
ms.assetid: c1a4aea8-8c48-4073-80ed-060db5adb514
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetModeInfo, GetModeInfo method [DirectShow], GetModeInfo method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetModeInfo method, IFullScreenVideoEx.GetModeInfo, IFullScreenVideoEx::GetModeInfo, IFullScreenVideoGetModeInfo, amvideo/IFullScreenVideoEx::GetModeInfo, dshow.ifullscreenvideoex_getmodeinfo
ms.topic: method
req.header: amvideo.h
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
 - IFullScreenVideoEx.GetModeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFullScreenVideoEx::GetModeInfo


## -description



The <code>GetModeInfo</code> method retrieves information about a specified display mode supported by the Full Screen Renderer filter.




## -parameters




### -param Mode [in]

Index of the display mode.


### -param pWidth [out]

Pointer to a variable that receives the width of the display mode, in pixels.


### -param pHeight [out]

Pointer to a variable that receives the height of the display mode, in pixels.


### -param pDepth [out]

Pointer to a variable that receives the bit depth of the display mode.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified display mode is not available and is disabled.

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
</table>
 




## -remarks



Display modes are indexed from zero. The <a href="https://msdn.microsoft.com/en-us/library/Dd390057(v=VS.85).aspx">IFullScreenVideoEx::CountModes</a> method returns the number of modes.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390056(v=VS.85).aspx">IFullScreenVideoEx Interface</a>
 

 

