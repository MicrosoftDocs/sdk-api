---
UID: NF:d3d9helper.IDirect3DDevice9.SetGammaRamp
title: IDirect3DDevice9::SetGammaRamp
author: windows-sdk-content
description: Sets the gamma correction ramp for the implicit swap chain. This method will affect the entire screen (not just the active window if you are running in windowed mode).
old-location: direct3d9\idirect3ddevice9__setgammaramp.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setgammaramp.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetGammaRamp method, IDirect3DDevice9.SetGammaRamp, IDirect3DDevice9::SetGammaRamp, SetGammaRamp, SetGammaRamp method [Direct3D 9], SetGammaRamp method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetGammaRamp, direct3d9.idirect3ddevice9__setgammaramp, e89cee81-1943-1a70-dd75-6de0d4b7dca7
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetGammaRamp


## -description


Sets the gamma correction ramp for the implicit swap chain. This method will affect the entire screen (not just the active window if you are running in windowed mode).


## -parameters




### -param iSwapChain [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Unsigned integer specifying the swap chain.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

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

Type: <b>const <a href="https://msdn.microsoft.com/c596f47a-6c09-4b97-ab2f-b1da3d851aa4">D3DGAMMARAMP</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/c596f47a-6c09-4b97-ab2f-b1da3d851aa4">D3DGAMMARAMP</a> structure, representing the gamma correction ramp to be set for the implicit swap chain. 


## -returns



No return value.




## -remarks



There is always at least one swap chain (the implicit swap chain) for each device, because Direct3D 9 has one swap chain as a property of the device. The gamma ramp takes effect immediately; there is no wait for a vertical sync.

If the device does not support gamma ramps in the swap chain's current presentation mode (full-screen or windowed), no error return is given. Applications can check the D3DCAPS2_FULLSCREENGAMMA and D3DCAPS2_CANCALIBRATEGAMMA capability bits in the Caps2 member of the D3DCAPS9 structure to determine the capabilities of the device and whether a calibrator is installed.

For windowed gamma correction presentation, use <a href="https://msdn.microsoft.com/ac90aee6-dd66-46d8-a628-4bf8bff087b4">IDirect3DSwapChain9::Present</a> if the hardware supports the feature. In DirectX 8, SetGammaRamp will set the gamma ramp only on a full-screen mode application. For more information about gamma correction, see <a href="https://msdn.microsoft.com/d076140d-3e91-412a-b099-9baa52f8d7d8">Gamma (Direct3D 9)</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/798ed6ed-ae8b-412d-b70b-024d198eb16f">IDirect3DDevice9::GetGammaRamp</a>



<a href="https://msdn.microsoft.com/df3fe9a0-cef9-4416-9287-4a1dd98b264d">IDirect3DSwapChain9</a>
 

 

