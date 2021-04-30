---
UID: NF:wingdi.wglSwapLayerBuffers
title: wglSwapLayerBuffers function (wingdi.h)
description: The wglSwapLayerBuffers function swaps the front and back buffers in the overlay, underlay, and main planes of the window referenced by a specified device context.
helpviewer_keywords: ["WGL_SWAP_MAIN_PLANE","WGL_SWAP_OVERLAYi","WGL_SWAP_UNDERLAYi","_ogl_wglSwapLayerBuffers","opengl.wglswaplayerbuffers","wglSwapLayerBuffers","wglSwapLayerBuffers function [OpenGL]","wingdi/wglSwapLayerBuffers"]
old-location: opengl\wglswaplayerbuffers.htm
tech.root: OpenGL
ms.assetid: e23a9ce3-8bb4-42e0-9460-170fa3949939
ms.date: 12/05/2018
ms.keywords: WGL_SWAP_MAIN_PLANE, WGL_SWAP_OVERLAYi, WGL_SWAP_UNDERLAYi, _ogl_wglSwapLayerBuffers, opengl.wglswaplayerbuffers, wglSwapLayerBuffers, wglSwapLayerBuffers function [OpenGL], wingdi/wglSwapLayerBuffers
req.header: wingdi.h
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
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - wglSwapLayerBuffers
 - wingdi/wglSwapLayerBuffers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - opengl32.dll
api_name:
 - wglSwapLayerBuffers
---

# wglSwapLayerBuffers function


## -description

The <b>wglSwapLayerBuffers</b> function swaps the front and back buffers in the overlay, underlay, and main planes of the window referenced by a specified device context.

## -parameters

### -param unnamedParam1

Specifies the device context of a window whose layer plane palette is to be realized into the physical palette.

### -param unnamedParam2

Specifies the overlay, underlay, and main planes whose front and back buffers are to be swapped. The <b>bReserved</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> structure specifies the number of overlay and underlay planes. The <i>fuPlanes</i> parameter is a bitwise combination of the following values.<div> </div>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WGL_SWAP_MAIN_PLANE"></a><a id="wgl_swap_main_plane"></a><dl>
<dt><b>WGL_SWAP_MAIN_PLANE</b></dt>
</dl>
</td>
<td width="60%">
Swaps the front and back buffers of the main plane.

</td>
</tr>
<tr>
<td width="40%"><a id="WGL_SWAP_OVERLAYi"></a><a id="wgl_swap_overlayi"></a><a id="WGL_SWAP_OVERLAYI"></a><dl>
<dt><b>WGL_SWAP_OVERLAYi</b></dt>
</dl>
</td>
<td width="60%">
Swaps the front and back buffers of the overlay plane <i>i</i>, where <i>i</i> is an integer between 1 and 15. WGL_SWAP_OVERLAY1 identifies the first overlay plane over the main plane, WGL_SWAP_OVERLAY2 identifies the second overlay plane over the first overlay plane, and so on.

</td>
</tr>
<tr>
<td width="40%"><a id="WGL_SWAP_UNDERLAYi"></a><a id="wgl_swap_underlayi"></a><a id="WGL_SWAP_UNDERLAYI"></a><dl>
<dt><b>WGL_SWAP_UNDERLAYi</b></dt>
</dl>
</td>
<td width="60%">
Swaps the front and back buffers of the underlay plane <i>i</i>, where <i>i</i> is an integer between 1 and 15. WGL_SWAP_UNDERLAY1 identifies the first underlay plane under the main plane, WGL_SWAP_UNDERLAY2 identifies the second underlay plane under the first underlay plane, and so on.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When a layer plane doesn't include a back buffer, calling the <b>wglSwapLayerBuffers</b> function has no effect on that layer plane. After you call <b>wglSwapLayerBuffers</b>, the state of the back buffer content is given in the corresponding <b>LAYERPLANEDESCRIPTOR</b> structure of the layer plane or in the <b>PIXELFORMATDESCRIPTOR</b> structure of the main plane. The <b>wglSwapLayerBuffers</b> function swaps the front and back buffers in the specified layer planes simultaneously.

Some devices don't support swapping layer planes individually; they swap all layer planes as a group. When the PFD_SWAP_LAYER_BUFFERS flag of the <b>PIXELFORMATDESCRIPTOR</b> structure is set, it indicates that a device can swap individual layer planes and that you can call <b>wglSwapLayerBuffers</b>.

With applications that use multiple threads, before calling <b>wglSwapLayerBuffers</b>, clear all drawing commands in all threads drawing to the same window.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-layerplanedescriptor">LAYERPLANEDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-swapbuffers">SwapBuffers</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>