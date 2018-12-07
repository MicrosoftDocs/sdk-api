---
UID: NF:dcomp.IDCompositionDevice2.CreateVirtualSurface
title: IDCompositionDevice2::CreateVirtualSurface
author: windows-sdk-content
description: Creates a sparsely populated surface that can be associated with one or more visuals for composition.
old-location: directcomp\idcompositiondevice2_createvirtualsurface.htm
tech.root: directcomp
ms.assetid: 659D79E3-2E7C-4431-B724-7AC2978BD9BC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateVirtualSurface, CreateVirtualSurface method [DirectComposition], CreateVirtualSurface method [DirectComposition],IDCompositionDevice2 interface, DXGI_ALPHA_MODE_IGNORE, DXGI_ALPHA_MODE_PREMULTIPLIED, DXGI_ALPHA_MODE_UNSPECIFIED, IDCompositionDevice2 interface [DirectComposition],CreateVirtualSurface method, IDCompositionDevice2.CreateVirtualSurface, IDCompositionDevice2::CreateVirtualSurface, dcomp/IDCompositionDevice2::CreateVirtualSurface, directcomp.idcompositiondevice2_createvirtualsurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice2.CreateVirtualSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice2::CreateVirtualSurface


## -description



        Creates a sparsely populated surface that can be associated with one or more visuals for composition.
      


## -parameters




### -param initialWidth [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The width of the surface, in pixels. The maximum width is 16,777,216 pixels.


### -param initialHeight [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The height of the surface, in pixels. The maximum height is 16,777,216 pixels.


### -param pixelFormat [in]

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

The pixel format of the surface.


### -param alphaMode [in]

Type: <b><a href="https://msdn.microsoft.com/DD3D1E49-06D2-4FB9-A41B-86453D8E566F">DXGI_ALPHA_MODE</a></b>

The meaning of the alpha channel, if the pixel format contains an alpha channel. It can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXGI_ALPHA_MODE_UNSPECIFIED"></a><a id="dxgi_alpha_mode_unspecified"></a><dl>
<dt><b>DXGI_ALPHA_MODE_UNSPECIFIED</b></dt>
</dl>
</td>
<td width="60%">
The alpha channel is not specified. This value has the same effect as <b>DXGI_ALPHA_MODE_IGNORE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="DXGI_ALPHA_MODE_PREMULTIPLIED"></a><a id="dxgi_alpha_mode_premultiplied"></a><dl>
<dt><b>DXGI_ALPHA_MODE_PREMULTIPLIED</b></dt>
</dl>
</td>
<td width="60%">
The color channels contain values that are premultiplied with the alpha channel.


</td>
</tr>
<tr>
<td width="40%"><a id="DXGI_ALPHA_MODE_IGNORE"></a><a id="dxgi_alpha_mode_ignore"></a><dl>
<dt><b>DXGI_ALPHA_MODE_IGNORE</b></dt>
</dl>
</td>
<td width="60%">
The alpha channel should be ignored and the bitmap should be rendered opaquely.

</td>
</tr>
</table>
 


### -param virtualSurface [out]

Type: <b><a href="https://msdn.microsoft.com/51E8D52C-2446-46B6-A5C1-0DC7FA9DF4CC">IDCompositionVirtualSurface</a>**</b>

The newly created surface object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A Microsoft DirectComposition sparse surface is a logical object that behaves like a rectangular array of pixels that can be associated with a visual for composition. The surface is not necessarily backed by any physical video or system memory for every one of its pixels. The application can realize or virtualize parts of the logical surface at different times.



A newly created surface object is in an uninitialized state. While it is uninitialized, the surface has no effect on the composition of the visual tree. It behaves exactly like a surface that is initialized with 100% transparent pixels. 

To initialize the surface with pixel data, use the <a href="https://msdn.microsoft.com/0D7E90A1-90E4-44BE-A4DA-8DA300C81A35">IDCompositionSurface::BeginDraw</a> and <a href="https://msdn.microsoft.com/127195F7-6000-4D8C-B850-3E4D40BC4082">IDCompositionSurface::EndDraw</a> methods. This method not only provides pixels for the surface, but it also allocates actual storage space for those pixels. The memory allocation persists until the application returns some of the memory to the system. The application can free part or all of the allocated memory by calling the <a href="https://msdn.microsoft.com/5A4F516F-B031-47E6-9A3D-068CF2C3D53A">IDCompositionVirtualSurface::Trim</a> method.

DirectComposition surfaces support the following pixel formats:

<ul>
<li><b>DXGI_FORMAT_B8G8R8A8_UNORM</b></li>
<li><b>DXGI_FORMAT_R8G8B8A8_UNORM</b></li>
<li><b>DXGI_FORMAT_R16G16B16A16_FLOAT</b></li>
</ul>
This method fails if <i>initialWidth</i> or <i>initialHeight</i> exceeds 16,777,216 pixels. 




## -see-also




<a href="https://msdn.microsoft.com/0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0">IDCompositionDevice2</a>



<a href="https://msdn.microsoft.com/3B321BF8-A7A5-4E40-B548-D88CA45F6DAF">IDCompositionDevice::CreateSurface</a>
 

 

