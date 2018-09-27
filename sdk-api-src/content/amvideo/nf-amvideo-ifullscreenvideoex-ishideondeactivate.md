---
UID: NF:amvideo.IFullScreenVideoEx.IsHideOnDeactivate
title: IFullScreenVideoEx::IsHideOnDeactivate
author: windows-sdk-content
description: The IsHideOnDeactivate method indicates the behavior when the user switches to another application.
old-location: dshow\ifullscreenvideoex_ishideondeactivate.htm
tech.root: DirectShow
ms.assetid: 0196215f-4efe-418a-acf3-445b8224a2ab
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],IsHideOnDeactivate method, IFullScreenVideoEx.IsHideOnDeactivate, IFullScreenVideoEx::IsHideOnDeactivate, IFullScreenVideoIsHideOnDeactivate, IsHideOnDeactivate, IsHideOnDeactivate method [DirectShow], IsHideOnDeactivate method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::IsHideOnDeactivate, dshow.ifullscreenvideoex_ishideondeactivate
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
 - IFullScreenVideoEx.IsHideOnDeactivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFullScreenVideoEx::IsHideOnDeactivate


## -description



The <code>IsHideOnDeactivate</code> method indicates the behavior when the user switches to another application. Depending on the setting, the full-screen video window is either minimized or hidden. If it is minimized, it appears as an icon in the task bar; otherwise, it does not.




## -parameters






## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The video window is minimized. (Default)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The video window is hidden.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

