---
UID: NS:d3d9types._D3DPRESENT_PARAMETERS_
title: "_D3DPRESENT_PARAMETERS_"
author: windows-driver-content
description: Describes the presentation parameters.
old-location: direct3d9\d3dpresent_parameters.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dpresent_parameters.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DPRESENT_PARAMETERS, D3DPRESENT_PARAMETERS structure [Direct3D 9], LPD3DPRESENT_PARAMETERS, LPD3DPRESENT_PARAMETERS structure pointer [Direct3D 9], _D3DPRESENT_PARAMETERS_, d3d9types/D3DPRESENT_PARAMETERS, d3d9types/LPD3DPRESENT_PARAMETERS, direct3d9.d3dpresent_parameters, f7919eb2-019d-9954-51ed-05071cd2587b
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: D3DPRESENT_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DPRESENT_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DPRESENT_PARAMETERS_ structure


## -description


Describes the presentation parameters.


## -struct-fields




### -field BackBufferWidth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the new swap chain's back buffers, in pixels. If <b>Windowed</b> is <b>FALSE</b> (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through <a href="https://msdn.microsoft.com/2e86d5bf-c7ac-47a8-af6c-0cd953d4cfa0">EnumAdapterModes</a>. If <b>Windowed</b> is <b>TRUE</b> and either <b>BackBufferWidth</b> or <b>BackBufferHeight</b> is zero, the corresponding dimension of the client area of the <b>hDeviceWindow</b> (or the focus window, if <b>hDeviceWindow</b> is <b>NULL</b>) is taken.


### -field BackBufferHeight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the new swap chain's back buffers, in pixels. If <b>Windowed</b> is <b>FALSE</b> (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through <a href="https://msdn.microsoft.com/2e86d5bf-c7ac-47a8-af6c-0cd953d4cfa0">EnumAdapterModes</a>. If <b>Windowed</b> is <b>TRUE</b> and either <b>BackBufferWidth</b> or <b>BackBufferHeight</b> is zero, the corresponding dimension of the client area of the <b>hDeviceWindow</b> (or the focus window, if <b>hDeviceWindow</b> is <b>NULL</b>) is taken.


### -field BackBufferFormat

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

The back buffer format. For more information about formats, see <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>. This value must be one of the render-target formats as validated by <a href="https://msdn.microsoft.com/bd19079c-d0ee-4e2f-8a02-9f26c8abcb31">CheckDeviceType</a>. You can use <a href="https://msdn.microsoft.com/6a96215a-366d-4820-9d9c-440673f1ef75">GetDisplayMode</a> to obtain the current format.

In fact, D3DFMT_UNKNOWN can be specified for the <b>BackBufferFormat</b> while in windowed mode. This tells the runtime to use the current display-mode format and eliminates the need to call <a href="https://msdn.microsoft.com/6a96215a-366d-4820-9d9c-440673f1ef75">GetDisplayMode</a>.

For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion). The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format. (There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)

Full-screen applications cannot do color conversion.


### -field BackBufferCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

This value can be between 0 and <a href="https://msdn.microsoft.com/47843a7a-619b-40ba-8111-56e021865353">D3DPRESENT_BACK_BUFFERS_MAX</a> (or <a href="https://msdn.microsoft.com/47843a7a-619b-40ba-8111-56e021865353">D3DPRESENT_BACK_BUFFERS_MAX_EX</a> when using Direct3D 9Ex). Values of 0 are treated as 1. If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created. As a result, an application can call the method twice with the same D3DPRESENT_PARAMETERS structure and expect it to work the second time.

The method fails if one back buffer cannot be created. The value of <b>BackBufferCount</b> influences what set of swap effects are allowed. Specifically, any D3DSWAPEFFECT_COPY swap effect requires that there be exactly one back buffer.


### -field MultiSampleType

Type: <b><a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a> enumerated type. The value must be D3DMULTISAMPLE_NONE unless <b>SwapEffect</b> has been set to D3DSWAPEFFECT_DISCARD. Multisampling is supported only if the swap effect is D3DSWAPEFFECT_DISCARD.


### -field MultiSampleQuality

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Quality level. The valid range is between zero and one less than the level returned by pQualityLevels used by  <a href="https://msdn.microsoft.com/82f1f1f6-0d9b-497b-b532-0d2aabbd0314">CheckDeviceMultiSampleType</a>. Passing a larger value returns the error D3DERR_INVALIDCALL. Paired values of render targets or of depth stencil surfaces and <a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a> must match.


### -field SwapEffect

Type: <b><a href="https://msdn.microsoft.com/522a5f71-3ad9-4cfc-a899-e25b9b721b1b">D3DSWAPEFFECT</a></b>

Member of the <a href="https://msdn.microsoft.com/522a5f71-3ad9-4cfc-a899-e25b9b721b1b">D3DSWAPEFFECT</a> enumerated type. The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if <b>Windowed</b> is <b>TRUE</b> and <b>SwapEffect</b> is set to D3DSWAPEFFECT_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.

D3DSWAPEFFECT_COPY requires that <b>BackBufferCount</b> be set to 1.

D3DSWAPEFFECT_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.

<table>
<tr>
<td>
Differences between Direct3D9 and Direct3D9Ex

In Direct3D9Ex, D3DSWAPEFFECT_FLIPEX is added to designate when an application is adopting flip mode. That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition. Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics. It does not change full screen behavior. Flip mode behavior is available beginning with Windows 7.

</td>
</tr>
</table>
 


### -field hDeviceWindow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The device window determines the location and size of the back buffer on screen. This is used by Direct3D when the back buffer contents are copied to the front buffer during <a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">Present</a>.

<ul>
<li>
For a full-screen application, this is a handle to the top window (which is the focus window). 

For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window. All other devices must have unique device windows.

</li>
<li>For a windowed-mode application, this handle will be the default target window for <a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">Present</a>. If this handle is <b>NULL</b>, the focus window will be taken.</li>
</ul>
Note that no attempt is made by the runtime to reflect user changes in window size. The back buffer is not implicitly reset when this window is reset. However, the <a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">Present</a> method does automatically track window position changes.


### -field Windowed

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the application runs windowed; <b>FALSE</b> if the application runs full-screen.


### -field EnableAutoDepthStencil

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If this value is <b>TRUE</b>, Direct3D will manage depth buffers for the application. The device will create a depth-stencil buffer when it is created. The depth-stencil buffer will be automatically set as the render target of the device. When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.

If EnableAutoDepthStencil is <b>TRUE</b>, then AutoDepthStencilFormat must be a valid depth-stencil format.


### -field AutoDepthStencilFormat

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type. The format of the automatic depth-stencil surface that the device will create. This member is ignored unless <b>EnableAutoDepthStencil</b> is <b>TRUE</b>.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

One of the <a href="https://msdn.microsoft.com/1294171e-b3f6-4264-8411-b69427cefe7b">D3DPRESENTFLAG</a> constants.


### -field FullScreen_RefreshRateInHz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The rate at which the display adapter refreshes the screen. The value depends on the mode in which the application is running:

<ul>
<li>For windowed mode, the refresh rate must be 0.</li>
<li>For full-screen mode, the refresh rate is one of the refresh rates returned by <a href="https://msdn.microsoft.com/2e86d5bf-c7ac-47a8-af6c-0cd953d4cfa0">EnumAdapterModes</a>.</li>
</ul>

### -field PresentationInterval

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The maximum rate at which the swap chain's back buffers can be presented to the front buffer. For a detailed explanation of the modes and the intervals that are supported, see <a href="https://msdn.microsoft.com/a7d774c1-93c0-47d8-a8a7-e66e394726a3">D3DPRESENT</a>.


## -see-also




<a href="https://msdn.microsoft.com/d41b36f6-8481-47f8-bd38-8f51bc9ff9b8">CreateAdditionalSwapChain</a>



<a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">CreateDevice</a>



<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">Present</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
 

 

