---
UID: NF:amvideo.IFullScreenVideoEx.IsModeEnabled
title: IFullScreenVideoEx::IsModeEnabled
author: windows-driver-content
description: The IsModeEnabled method queries whether a specified display mode is enabled.
old-location: dshow\ifullscreenvideoex_ismodeenabled.htm
old-project: DirectShow
ms.assetid: 97d8b9f8-4dbf-4b49-b32f-4513c9e5186e
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],IsModeEnabled method, IFullScreenVideoEx.IsModeEnabled, IFullScreenVideoEx::IsModeEnabled, IFullScreenVideoIsModeEnabled, IsModeEnabled, IsModeEnabled method [DirectShow], IsModeEnabled method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::IsModeEnabled, dshow.ifullscreenvideoex_ismodeenabled
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IFullScreenVideoEx.IsModeEnabled
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IFullScreenVideoEx::IsModeEnabled


## -description



The <code>IsModeEnabled</code> method queries whether a specified display mode is enabled.




## -parameters




### -param Mode [in]

Index of the display mode to query.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The display mode is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The display mode is enabled.

</td>
</tr>
</table>
 




## -remarks



The Full Screen Renderer supports a static set of display modes. By default, every mode is enabled. You can enable or disable a display mode by calling the <a href="https://msdn.microsoft.com/f05c1b3e-3ebc-4753-b3ca-e52907c59121">IFullScreenVideoEx::SetEnabled</a>. The <b>IsEnabled</b> method retrieves the current setting for the specified mode.

The video card on the user's system might not support every mode. The Full Screen Renderer will not use a mode that the video card does not support, even if that mode is enabled. To determine whether the card supports a particular mode, call the <a href="https://msdn.microsoft.com/9b05d6c6-522c-46b8-90b5-c4650cee5f6b">IFullScreenVideoEx::IsModeAvailable</a> method. If a mode is disabled, the Full Screen Renderer will not use it, even if the card supports it.

Display modes are indexed from zero. The <a href="https://msdn.microsoft.com/70d4e124-083b-4729-8f39-778e815ea23b">IFullScreenVideoEx::CountModes</a> method returns the number of modes.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

