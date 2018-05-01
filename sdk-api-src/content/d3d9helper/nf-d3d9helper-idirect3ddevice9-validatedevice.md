---
UID: NF:d3d9helper.IDirect3DDevice9.ValidateDevice
title: IDirect3DDevice9::ValidateDevice method
author: windows-driver-content
description: Reports the device's ability to render the current texture-blending operations and arguments in a single pass.
old-location: direct3d9\idirect3ddevice9__validatedevice.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__validatedevice.htm
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: 8ca7b036-a40e-e1d7-8756-34204c874629, IDirect3DDevice9, IDirect3DDevice9 interface [Direct3D 9], ValidateDevice method, IDirect3DDevice9::ValidateDevice, ValidateDevice method [Direct3D 9], ValidateDevice method [Direct3D 9], IDirect3DDevice9 interface, ValidateDevice,IDirect3DDevice9.ValidateDevice, d3d9helper/IDirect3DDevice9::ValidateDevice, direct3d9.idirect3ddevice9__validatedevice
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DDevice9.ValidateDevice
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::ValidateDevice method


## -description


Reports the device's ability to render the current texture-blending operations and arguments in a single pass.


## -parameters




### -param pNumPasses [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer to a DWORD value to fill with the number of rendering passes needed to complete the desired effect through multipass rendering. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_CONFLICTINGRENDERSTATE, D3DERR_CONFLICTINGTEXTUREFILTER, D3DERR_DEVICELOST, D3DERR_DRIVERINTERNALERROR, D3DERR_TOOMANYOPERATIONS, D3DERR_UNSUPPORTEDALPHAARG, D3DERR_UNSUPPORTEDALPHAOPERATION, D3DERR_UNSUPPORTEDCOLORARG, D3DERR_UNSUPPORTEDCOLOROPERATION, D3DERR_UNSUPPORTEDFACTORVALUE, D3DERR_UNSUPPORTEDTEXTUREFILTER, D3DERR_WRONGTEXTUREFORMAT,.




## -remarks



The <b>IDirect3DDevice9::ValidateDevice</b> method should be used to validate scenarios only when other capabilities are deficient. For example, in a multistage texturing scenario, you could query the MaxTextureBlendStages and MaxSimultaneousTextures members of a <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure to determine if multistage texturing is possible on the device.

Current hardware does not necessarily implement all possible combinations of operations and arguments. You can determine whether a particular blending operation can be performed with given arguments by setting the desired blending operation, and then calling the <b>IDirect3DDevice9::ValidateDevice</b> method. 

The <b>IDirect3DDevice9::ValidateDevice</b> method uses the current render states, textures, and texture-stage states to perform validation at the time of the call. Changes to these factors after the call invalidate the previous result, and the method must be called again before rendering a scene.

For best performance, call <b>IDirect3DDevice9::ValidateDevice</b> at initialization time; do not use it within a render loop.

Using diffuse iterated values, either as an argument or as an operation (D3DTA_DIFFUSED3DTOP_BLENDDIFFUSEALPHA) is rarely supported on current hardware. Most hardware can introduce iterated color data only at the last texture operation stage.

Try to specify the texture (D3DTA_TEXTURE) for each stage as the first argument, rather than the second argument.

Many cards do not support use of diffuse or scalar values at arbitrary texture stages. Often, these are available only at the first or last texture-blending stage.

Many cards do not have a blending unit associated with the first texture that is capable of more than replicating alpha to color channels or inverting the input. Therefore, your application might need to use only the second texture stage, if possible. On such hardware, the first unit is presumed to be in its default state, which has the first color argument set to D3DTA_TEXTURE with the D3DTOP_SELECTARG1 operation.

Operations on the output alpha that are more intricate than or substantially different from the color operations are less likely to be supported. 

Some hardware does not support simultaneous use of D3DTA_TFACTOR and D3DTA_DIFFUSE.

Many cards do not support simultaneous use of multiple textures and mipmapped trilinear filtering. If trilinear filtering has been requested for a texture involved in multitexture blending operations and validation fails, turn off trilinear filtering and revalidate. In this case, you might want to perform multipass rendering instead.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/8ecc2019-16f9-4c32-9ecb-33c2b85108dc">IDirect3DDevice9::GetTextureStageState</a>



<a href="https://msdn.microsoft.com/303f7a80-edaf-4106-a4ce-8fb7a7d30a5a">IDirect3DDevice9::SetTextureStageState</a>
 

 

