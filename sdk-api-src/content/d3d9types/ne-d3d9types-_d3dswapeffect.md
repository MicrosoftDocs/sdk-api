---
UID: NE:d3d9types._D3DSWAPEFFECT
title: "_D3DSWAPEFFECT"
author: windows-driver-content
description: Defines swap effects.
old-location: direct3d9\D3DSWAPEFFECT.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dswapeffect.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 5157d683-19a1-eb9d-09f1-c480e6ed220e, D3DSWAPEFFECT, D3DSWAPEFFECT enumeration [Direct3D 9], D3DSWAPEFFECT_COPY, D3DSWAPEFFECT_DISCARD, D3DSWAPEFFECT_FLIP, D3DSWAPEFFECT_FLIPEX, D3DSWAPEFFECT_FORCE_DWORD, D3DSWAPEFFECT_OVERLAY, LPD3DSWAPEFFECT, LPD3DSWAPEFFECT enumeration pointer [Direct3D 9], _D3DSWAPEFFECT, d3d9types/D3DSWAPEFFECT, d3d9types/D3DSWAPEFFECT_COPY, d3d9types/D3DSWAPEFFECT_DISCARD, d3d9types/D3DSWAPEFFECT_FLIP, d3d9types/D3DSWAPEFFECT_FLIPEX, d3d9types/D3DSWAPEFFECT_FORCE_DWORD, d3d9types/D3DSWAPEFFECT_OVERLAY, d3d9types/LPD3DSWAPEFFECT, direct3d9.D3DSWAPEFFECT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d9types.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D3DSWAPEFFECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DSWAPEFFECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DSWAPEFFECT enumeration


## -description


Defines swap effects.


## -enum-fields




### -field D3DSWAPEFFECT_DISCARD

When a swap chain is created with a swap effect of D3DSWAPEFFECT_FLIP or  D3DSWAPEFFECT_COPY, the runtime will guarantee that an <a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">IDirect3DDevice9::Present</a> operation will not affect the content of any of the back buffers. Unfortunately, meeting this guarantee can involve substantial video memory or processing overheads, especially when implementing flip semantics for a windowed swap chain or copy semantics for a full-screen swap chain. An application may use the D3DSWAPEFFECT_DISCARD swap effect to avoid these overheads and to enable the display driver to select the most efficient presentation technique for the swap chain. This is also the only swap effect that may be used when specifying a value other than D3DMULTISAMPLE_NONE for the MultiSampleType member of <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>.

Like a swap chain that uses D3DSWAPEFFECT_FLIP, a swap chain that uses D3DSWAPEFFECT_DISCARD might include more than one back buffer, any of which may be accessed using <a href="https://msdn.microsoft.com/fac7f4eb-ce6f-4f9d-810c-f3a0ad155cc2">IDirect3DDevice9::GetBackBuffer</a> or <a href="https://msdn.microsoft.com/89fa363f-023d-43aa-8f09-fa80ac49ccb6">IDirect3DSwapChain9::GetBackBuffer</a>. The swap chain is best envisaged as a queue in which 0 always indexes the back buffer that will be displayed by the next Present operation and from which buffers are discarded when they have been displayed.

An application that uses this swap effect cannot make any assumptions about the contents of a discarded back buffer and should therefore update an entire back buffer before invoking a Present operation that would display it. Although this is not enforced, the debug version of the runtime will overwrite the contents of discarded back buffers with random data to enable developers to verify that their applications are updating the entire back buffer surfaces correctly.


### -field D3DSWAPEFFECT_FLIP

The swap chain might include multiple back buffers and is best envisaged as a circular queue that includes the front buffer. Within this queue, the back buffers are always numbered sequentially from 0 to (n - 1), where n is the number of back buffers, so that 0 denotes the least recently presented buffer. When Present is invoked, the queue is "rotated" so that the front buffer becomes back buffer (n - 1), while the back buffer 0 becomes the new front buffer.


### -field D3DSWAPEFFECT_COPY

This swap effect may be specified only for a swap chain comprising a single back buffer. Whether the swap chain is windowed or full-screen, the runtime will guarantee the semantics implied by a copy-based Present operation, namely that the operation leaves the content of the back buffer unchanged, instead of replacing it with the content of the front buffer as a flip-based Present operation would. 

For a full-screen swap chain, the runtime uses a combination of flip operations and copy operations, supported if necessary by hidden back buffers, to accomplish the Present operation. Accordingly, the presentation is synchronized with the display adapter's vertical retrace and its rate is constrained by the chosen presentation interval. A swap chain specified with the D3DPRESENT_INTERVAL_IMMEDIATE flag is the only exception. (Refer to the description of the <b>PresentationIntervals</b>
     member of the <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> structure.) In this case, a Present operation copies the back buffer content directly to the front buffer without waiting for the vertical retrace.


### -field D3DSWAPEFFECT_OVERLAY

Use a dedicated area of video memory that can be overlayed on the primary surface. No copy is performed when the overlay is displayed. 
      The overlay operation is performed in hardware, without modifying the data in the primary surface.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 9Ex:

D3DSWAPEFFECT_OVERLAY is only available in Direct3D9Ex running on Windows 7 (or more current operating system).

</td>
</tr>
</table>
 


### -field D3DSWAPEFFECT_FLIPEX

Designates when an application is adopting flip mode, during which time an application's frame is passed instead of copied to the Desktop Window Manager(DWM) for composition when the application is presenting in windowed mode. Flip mode allows an application to more efficiently use memory bandwidth as well as enabling an application to take advantage of full-screen-present statistics. Flip mode does not affect full-screen behavior. A sample application that uses <a href="https://msdn.microsoft.com/a7d774c1-93c0-47d8-a8a7-e66e394726a3">D3DPRESENT_FORCEIMMEDIATE</a> and D3DSWAPEFFECT_FLIPEX is the <a href="http://go.microsoft.com/fwlink/p/?linkid=179115">D3D9ExFlipEx sample on the MSDN Code Gallery</a>.

<div class="alert"><b>Note</b>  If you create a swap chain with D3DSWAPEFFECT_FLIPEX, you can't override the <b>hDeviceWindow</b> member of the <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> structure when you present a new frame for display. That is, you must pass <b>NULL</b> to the <i>hDestWindowOverride</i> parameter of <a href="https://msdn.microsoft.com/845c72ff-669d-44bf-8065-cff456418e8c">IDirect3DDevice9Ex::PresentEx</a> to instruct the runtime to use the <b>hDeviceWindow</b> member of <b>D3DPRESENT_PARAMETERS</b> for the presentation.</div>
<div> </div>
<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 9Ex:

D3DSWAPEFFECT_FLIPEX is only available in Direct3D9Ex running on Windows 7 (or more current operating system).

</td>
</tr>
</table>
 


### -field D3DSWAPEFFECT_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



The state of the back buffer after a call to Present is well-defined by each of these swap effects, and whether the Direct3D device was created with a full-screen swap chain or a windowed swap chain has no effect on this state. In particular, the D3DSWAPEFFECT_FLIP swap effect operates the same whether windowed or full-screen, and the Direct3D runtime guarantees this by creating extra buffers. As a result, it is recommended that applications use D3DSWAPEFFECT_DISCARD whenever possible to avoid any such penalties. This is because this swap effect will always be the most efficient in terms of memory consumption and performance.

Applications that use D3DSWAPEFFECT_FLIP or D3DSWAPEFFECT_DISCARD should not expect full-screen destination alpha to work. This means that the D3DRS_DESTBLEND render state will not work as expected because full-screen swap chains with these swap effects do not have an explicit pixel format from the driver's point of view. The driver infers that they should take on the display format, which does not have an alpha channel. To work around this, take the following steps: 

<ul>
<li>Use D3DSWAPEFFECT_COPY.</li>
<li>Check the D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD flag in the Caps3 member of the <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure. This flag indicates whether the driver can do alpha blending when D3DSWAPEFFECT_FLIP or D3DSWAPEFFECT_DISCARD is used.</li>
<li>Applications using flip mode swap effect (D3DSWAPEFFECT_FLIPEX) should call <a href="https://msdn.microsoft.com/845c72ff-669d-44bf-8065-cff456418e8c">PresentEx</a> after a window resize or region change to ensure that the display content is updated.</li>
</ul>
An invisible window cannot receive user-mode events; furthermore, an invisible-fullscreen window will interfere with the presentation of another applications' windowed-mode window. Therefore, each application needs to ensure that a device window is visible when a swapchain is presented in fullscreen mode.




## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/6d672f22-9843-4ff7-ae79-4903f56cd1e9">IDirect3DDevice9::Reset</a>
 

 

