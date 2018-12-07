---
UID: NF:d3d11.ID3D11Device.CreateHullShader
title: ID3D11Device::CreateHullShader
author: windows-sdk-content
description: Create a hull shader.
old-location: direct3d11\id3d11device_createhullshader.htm
tech.root: direct3d11
ms.assetid: 93ec9f46-69c5-4863-bd74-9c8c92fae586
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 3183fc89-b12c-d245-312b-a06f19ecd6de, CreateHullShader, CreateHullShader method [Direct3D 11], CreateHullShader method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateHullShader method, ID3D11Device.CreateHullShader, ID3D11Device::CreateHullShader, d3d11/ID3D11Device::CreateHullShader, direct3d11.id3d11device_createhullshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreateHullShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device::CreateHullShader


## -description


Create a <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">hull shader</a>.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to a compiled shader.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled shader.


### -param pClassLinkage [in, optional]

Type: <b><a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>*</b>

A pointer to a class linkage interface (see <a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>); the value can be <b>NULL</b>.


### -param ppHullShader [out, optional]

Type: <b><a href="https://msdn.microsoft.com/3459f533-e2ac-4b0e-bfdd-d9dae704f418">ID3D11HullShader</a>**</b>

Address of a pointer to a <a href="https://msdn.microsoft.com/3459f533-e2ac-4b0e-bfdd-d9dae704f418">ID3D11HullShader</a> interface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



The Direct3D 11.1 runtime, which is available starting with Windows 8, provides the following new functionality for <b>CreateHullShader</b>.

The following shader model 5.0 instructions are available to just pixel shaders and compute shaders in the Direct3D 11.0 runtime. For the Direct3D 11.1 runtime, because unordered access views (UAV) are available at all shader stages, you can use these instructions in all shader stages.

Therefore, if you use the following shader model 5.0 instructions in a hull shader, you can successfully pass the compiled hull shader to <i>pShaderBytecode</i>. That is, the call to <b>CreateHullShader</b> succeeds.

If you pass a compiled shader to <i>pShaderBytecode</i> that uses any of the following instructions on a device that doesn’t support UAVs at every shader stage (including existing drivers that are not implemented to support UAVs at every shader stage), <b>CreateHullShader</b> fails.  <b>CreateHullShader</b> also fails if the shader tries to use a UAV slot beyond the set of UAV slots that the hardware supports.

<ul>
<li>
<a href="https://msdn.microsoft.com/F9F5583F-E3D0-447F-9227-BBB1B4E71934">dcl_uav_typed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/D0F43FF8-FF1C-4E42-AF42-F528C98FD680">dcl_uav_raw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B">dcl_uav_structured</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447155(v=VS.85).aspx">ld_raw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447157(v=VS.85).aspx">ld_structured</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447160(v=VS.85).aspx">ld_uav_typed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447236(v=VS.85).aspx">store_raw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447237(v=VS.85).aspx">store_structured</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447238(v=VS.85).aspx">store_uav_typed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447241(v=VS.85).aspx">sync_uglobal</a>
</li>
<li>All atomics and immediate atomics (for example, <a href="https://msdn.microsoft.com/en-us/library/Hh446819(v=VS.85).aspx">atomic_and</a> and <a href="https://msdn.microsoft.com/en-us/library/Hh447118(v=VS.85).aspx">imm_atomic_and</a>)</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>
 

 

