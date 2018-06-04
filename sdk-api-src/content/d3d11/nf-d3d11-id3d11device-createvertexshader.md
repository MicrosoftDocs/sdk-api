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

# ID3D11Device::CreateVertexShader


## -description


Create a vertex-shader object from a compiled shader.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. 


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled vertex shader.


### -param pClassLinkage [in, optional]

Type: <b><a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>*</b>

A pointer to a class linkage interface (see <a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>); the value can be <b>NULL</b>.


### -param ppVertexShader [out, optional]

Type: <b><a href="https://msdn.microsoft.com/8300ec12-ecf5-49c2-9313-b542a7d971f3">ID3D11VertexShader</a>**</b>

Address of a pointer to a <a href="https://msdn.microsoft.com/8300ec12-ecf5-49c2-9313-b542a7d971f3">ID3D11VertexShader</a> interface. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return <b>S_FALSE</b> instead of <b>S_OK</b>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



The Direct3D 11.1 runtime, which is available starting with Windows 8, provides the following new functionality for <b>CreateVertexShader</b>.

The following shader model 5.0 instructions are available to just pixel shaders and compute shaders in the Direct3D 11.0 runtime. For the Direct3D 11.1 runtime, because unordered access views (UAV) are available at all shader stages, you can use these instructions in all shader stages.

Therefore, if you use the following shader model 5.0 instructions in a vertex shader, you can successfully pass the compiled vertex shader to <i>pShaderBytecode</i>. That is, the call to <b>CreateVertexShader</b> succeeds.

If you pass a compiled shader to <i>pShaderBytecode</i> that uses any of the following instructions on a device that doesn’t support UAVs at every shader stage (including existing drivers that are not implemented to support UAVs at every shader stage), <b>CreateVertexShader</b> fails.  <b>CreateVertexShader</b> also fails if the shader tries to use a UAV slot beyond the set of UAV slots that the hardware supports.

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
<a href="https://msdn.microsoft.com/F7DBA80D-4DD5-4271-B571-24FB6188ABFE">ld_raw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ED572B76-FF6C-405E-9110-4B12AD5E5AE6">ld_structured</a>
</li>
<li>
<a href="https://msdn.microsoft.com/E5E03311-3596-4497-9271-FE6445DBFC62">ld_uav_typed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/D166116A-CF4E-4020-9F6A-F9CEEFCDAB21">store_raw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF">store_structured</a>
</li>
<li>
<a href="https://msdn.microsoft.com/AD8E035B-DACD-4241-A05B-7D6DC8E3222C">store_uav_typed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/DCA637FE-8F5C-41D0-8B5E-F913463BA387">sync_uglobal</a>
</li>
<li>All atomics and immediate atomics (for example, <a href="https://msdn.microsoft.com/5FA731E0-7D18-4416-9579-FCA01FF5FC38">atomic_and</a> and <a href="https://msdn.microsoft.com/DA2A70C3-57BD-41F0-865C-235AA4DF1A52">imm_atomic_and</a>)</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

