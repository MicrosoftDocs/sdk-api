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

# IDirect3DDevice9::SetViewport


## -description


Sets the viewport parameters for the device.


## -parameters




### -param pViewport [in]

Type: <b>const <a href="https://msdn.microsoft.com/fb2c6048-f837-497d-8e4f-e18942d37899">D3DVIEWPORT9</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/fb2c6048-f837-497d-8e4f-e18942d37899">D3DVIEWPORT9</a> structure, specifying the viewport parameters to set. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, it will return D3DERR_INVALIDCALL. This will happen if pViewport is invalid, or if pViewport describes a region that cannot exist within the render target surface.




## -remarks



Direct3D sets the following default values for the viewport.



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
D3DVIEWPORT9 vp;
vp.X      = 0;
vp.Y      = 0;
vp.Width  = RenderTarget.Width;
vp.Height = RenderTarget.Height;
vp.MinZ   = 0.0f;
vp.MaxZ   = 1.0f;
</pre>
</td>
</tr>
</table></span></div>
<b>IDirect3DDevice9::SetViewport</b> can be used to draw on part of the screen. Make sure to call it before any geometry is drawn so the viewport settings will take effect.

To draw multiple views within a scene, repeat the <b>IDirect3DDevice9::SetViewport</b> and draw geometry sequence for each view.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/026da206-b2e7-421c-92f8-344fef7ad245">IDirect3DDevice9::GetViewport</a>
 

 

