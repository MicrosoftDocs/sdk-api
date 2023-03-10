---
UID: NF:d3d9helper.IDirect3DDevice9.SetGammaRamp
title: IDirect3DDevice9::SetGammaRamp (d3d9helper.h)
description: The IDirect3DDevice9::SetGammaRamp method (d3d9helper.h) sets the gamma correction ramp for the implicit swap chain.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetGammaRamp method","IDirect3DDevice9.SetGammaRamp","IDirect3DDevice9::SetGammaRamp","SetGammaRamp","SetGammaRamp method [Direct3D 9]","SetGammaRamp method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetGammaRamp","direct3d9.idirect3ddevice9__setgammaramp","e89cee81-1943-1a70-dd75-6de0d4b7dca7"]
old-location: direct3d9\idirect3ddevice9__setgammaramp.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setgammaramp.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetGammaRamp method, IDirect3DDevice9.SetGammaRamp, IDirect3DDevice9::SetGammaRamp, SetGammaRamp, SetGammaRamp method [Direct3D 9], SetGammaRamp method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetGammaRamp, direct3d9.idirect3ddevice9__setgammaramp, e89cee81-1943-1a70-dd75-6de0d4b7dca7
req.header: d3d9helper.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::SetGammaRamp
 - d3d9helper/IDirect3DDevice9::SetGammaRamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.SetGammaRamp
---

# IDirect3DDevice9::SetGammaRamp


## -description

Sets the gamma correction ramp for the implicit swap chain. This method will affect the entire screen (not just the active window if you are running in windowed mode).

## -parameters

### -param iSwapChain [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Unsigned integer specifying the swap chain.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Indicates whether correction should be applied. Gamma correction results in a more consistent display, but can incur processing overhead and should not be used frequently. Short-duration effects, such as flashing the whole screen red, should not be calibrated, but long-duration gamma changes should be calibrated. One of the following values can be set: 



<table>
<tr>
<th>Item</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="D3DSGR_CALIBRATE"></a><a id="d3dsgr_calibrate"></a>D3DSGR_CALIBRATE

</td>
<td width="60%">
If a gamma calibrator is installed, the ramp will be modified before being sent to the device to account for the system and monitor response curves. If a calibrator is not installed, the ramp will be passed directly to the device.

</td>
</tr>
<tr>
<td width="40%">
<a id="D3DSGR_NO_CALIBRATION"></a><a id="d3dsgr_no_calibration"></a>D3DSGR_NO_CALIBRATION

</td>
<td width="60%">
No gamma correction is applied. The supplied gamma table is transferred directly to the device.

</td>
</tr>
</table>

### -param pRamp [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3dgammaramp">D3DGAMMARAMP</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dgammaramp">D3DGAMMARAMP</a> structure, representing the gamma correction ramp to be set for the implicit swap chain.

## -remarks

There is always at least one swap chain (the implicit swap chain) for each device, because Direct3D 9 has one swap chain as a property of the device. The gamma ramp takes effect immediately; there is no wait for a vertical sync.

If the device does not support gamma ramps in the swap chain's current presentation mode (full-screen or windowed), no error return is given. Applications can check the D3DCAPS2_FULLSCREENGAMMA and D3DCAPS2_CANCALIBRATEGAMMA capability bits in the Caps2 member of the D3DCAPS9 structure to determine the capabilities of the device and whether a calibrator is installed.

For windowed gamma correction presentation, use <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present">IDirect3DSwapChain9::Present</a> if the hardware supports the feature. In DirectX 8, SetGammaRamp will set the gamma ramp only on a full-screen mode application. For more information about gamma correction, see <a href="/windows/desktop/direct3d9/gamma">Gamma (Direct3D 9)</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getgammaramp">IDirect3DDevice9::GetGammaRamp</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a>
