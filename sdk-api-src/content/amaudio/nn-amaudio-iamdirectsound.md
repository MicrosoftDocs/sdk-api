---
UID: NN:amaudio.IAMDirectSound
title: IAMDirectSound (amaudio.h)
author: windows-sdk-content
description: The IAMDirectSound interface specifies which window has focus for controlling DirectSound audio playback.
old-location: dshow\iamdirectsound.htm
tech.root: DirectShow
ms.assetid: a9afaeb7-e2d4-4dbf-9f4d-144cafbd5e28
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMDirectSound, IAMDirectSound interface [DirectShow], IAMDirectSound interface [DirectShow],described, IAMDirectSoundInterface, amaudio/IAMDirectSound, dshow.iamdirectsound
ms.topic: interface
req.header: amaudio.h
req.include-header: 
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
 - IAMDirectSound
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMDirectSound interface


## -description



The <code>IAMDirectSound</code> interface specifies which window has focus for controlling DirectSound audio playback. DirectShow provides limited support for this interface:

<ul>
<li>The <a href="https://msdn.microsoft.com/ec6cc790-8c1f-4de4-a7ca-a7073894380e">DirectSound Renderer</a> implements the <b>GetFocusWindow</b> and <b>SetFocusWindow</b> methods. It does not implement the other methods on the interface.</li>
<li>The <a href="https://msdn.microsoft.com/a3f2776b-974b-4886-82a3-38e00b607a07">Audio Renderer (WaveOut)</a> exposes the interface but does not implement any of its methods.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMDirectSound</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMDirectSound</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMDirectSound</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389194(v=VS.85).aspx">GetDirectSoundInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389195(v=VS.85).aspx">GetFocusWindow</a>
</td>
<td align="left" width="63%">
Retrieves the window that is handling sound playback for the current media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389196(v=VS.85).aspx">GetPrimaryBufferInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389306(v=VS.85).aspx">GetSecondaryBufferInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389307(v=VS.85).aspx">ReleaseDirectSoundInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389308(v=VS.85).aspx">ReleasePrimaryBufferInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389309(v=VS.85).aspx">ReleaseSecondaryBufferInterface</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389310(v=VS.85).aspx">SetFocusWindow</a>
</td>
<td align="left" width="63%">
Sets the window that will handle sound playback for the current media file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

