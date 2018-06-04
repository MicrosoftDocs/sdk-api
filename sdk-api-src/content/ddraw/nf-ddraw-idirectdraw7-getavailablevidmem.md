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

# IDirectDraw7::GetAvailableVidMem


## -description


Retrieves the total amount of display memory available and the amount of display memory currently free for a given type of surface.


## -parameters




### -param






#### - lpDDSCaps2 [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a> structure that indicates the hardware capabilities of the proposed surface.


#### - lpdwFree [out]

A pointer to a variable that receives the amount of display memory currently free that can be allocated for a surface that matches the capabilities specified by the structure at <i>lpDDSCaps2</i>.


#### - lpdwTotal [out]

A pointer to a variable that receives the total amount of display memory available, in bytes. The value received reflects the total video memory, minus the video memory required for the primary surface and any private caches that the display driver reserves.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDCAPS</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NODIRECTDRAWHW</li>
</ul>



## -remarks



The following C++ example demonstrates how to use <b>GetAvailableVidMem</b> to determine both the total and free display memory available for texture-map surfaces:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>// For this example, the lpDD variable is a valid 
// pointer to an IDirectDraw7 interface.
LPDIRECTDRAW7 lpDD;
DDSCAPS2      ddsCaps2; 
DWORD         dwTotal; 
DWORD         dwFree;
HRESULT       hr; 
 
hr = lpDD-&gt;QueryInterface(IID_IDirectDraw7, &amp;lpDD); 
if (FAILED(hr))
    return hr; 
 
// Initialize the structure.
ZeroMemory(&amp;ddsCaps2, sizeof(ddsCaps2));
 
ddsCaps2.dwCaps = DDSCAPS_TEXTURE; 
hr = lpDD-&gt;GetAvailableVidMem(&amp;ddsCaps2, &amp;dwTotal, &amp;dwFree); 
if (FAILED(hr))
    return hr;

</pre>
</td>
</tr>
</table></span></div>
If the surface has the <a href="ddscaps.htm">DDSCAPS_VIDEOMEMORY</a> flag set, <b>GetAvailableVidMem</b> returns different amounts of video memory depending on whether the surface can be used as a 3-D texture. If the surface can be used for 3-D textures, <b>GetAvailableVidMem</b> returns the sum of the local video memory and the non-local video memory on AGP systems.

<b>GetAvailableVidMem</b> provides only a snapshot of the current display-memory state. The amount of free display memory is subject to change as surfaces are created and released. Therefore, you should use the free memory value only as an approximation. In addition, a particular display adapter card might make no distinction between two different memory types. For example, the adapter might use the same portion of display memory to store z-buffers and textures. So, allocating one type of surface (for example, a z-buffer) can affect the amount of display memory available for another type of surface (textures). Therefore, it is best to first allocate an application's fixed resources (such as front and back buffers and z-buffers) before determining how much memory is available for dynamic use (such as texture mapping).



<b>GetAvailableVidMem</b> was not implemented in the previous DirectX IDirectDraw interface version.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetAvailableVidMem</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

