---
UID: NF:d3d11.ID3D11Device.CreateGeometryShader
title: ID3D11Device::CreateGeometryShader
author: windows-sdk-content
description: Create a geometry shader.
old-location: direct3d11\id3d11device_creategeometryshader.htm
old-project: direct3d11
ms.assetid: fb9357d7-ac63-4515-9118-24a2d775e697
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: CreateGeometryShader, CreateGeometryShader method [Direct3D 11], CreateGeometryShader method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateGeometryShader method, ID3D11Device.CreateGeometryShader, ID3D11Device::CreateGeometryShader, c0fe27f5-e83c-fa7e-faca-a34ea90a0c53, d3d11/ID3D11Device::CreateGeometryShader, direct3d11.id3d11device_creategeometryshader
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreateGeometryShader
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CreateGeometryShader


## -description


Create a geometry shader.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. 
        


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Size of the compiled geometry shader.


### -param pClassLinkage [in, optional]

Type: <b><a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>*</b>

A pointer to a class linkage interface (see <a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>); the value can be <b>NULL</b>.


### -param ppGeometryShader [out, optional]

Type: <b><a href="https://msdn.microsoft.com/c2b5863d-5773-4719-b1d0-2026f55fcef3">ID3D11GeometryShader</a>**</b>

Address of a pointer to a <a href="https://msdn.microsoft.com/c2b5863d-5773-4719-b1d0-2026f55fcef3">ID3D11GeometryShader</a> interface. If this is <b>NULL</b>, all other parameters will be validated, and if all
        parameters pass validation this API will return S_FALSE instead of S_OK.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



After it is created, the shader can be set to the device by calling <a href="https://msdn.microsoft.com/6c42d028-b832-470c-ab15-1cf46a3f8414">ID3D11DeviceContext::GSSetShader</a>.

The Direct3D 11.1 runtime, which is available starting with Windows 8, provides the following new functionality for <b>CreateGeometryShader</b>.

The following shader model 5.0 instructions are available to just pixel shaders and compute shaders in the Direct3D 11.0 runtime. For the Direct3D 11.1 runtime, because unordered access views (UAV) are available at all shader stages, you can use these instructions in all shader stages.

Therefore, if you use the following shader model 5.0 instructions in a geometry shader, you can successfully pass the compiled geometry shader to <i>pShaderBytecode</i>. That is, the call to <b>CreateGeometryShader</b> succeeds.

If you pass a compiled shader to <i>pShaderBytecode</i> that uses any of the following instructions on a device that doesn’t support UAVs at every shader stage (including existing drivers that are not implemented to support UAVs at every shader stage), <b>CreateGeometryShader</b> fails.  <b>CreateGeometryShader</b> also fails if the shader tries to use a UAV slot beyond the set of UAV slots that the hardware supports.

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

#### Examples


          Usage Example

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
ID3D11GeometryShader*       g_pGeometryShader11 = NULL;
ID3DBlob* pGeometryShaderBuffer = NULL;
ID3DBlob * errorbuffer = NULL;

D3DX11CompileFromFile( str, NULL, NULL, "GS", "gs_4_0", dwShaderFlags, 0, NULL,
                                         &amp;pGeometryShaderBuffer, &amp;errorbuffer, NULL );

pd3dDevice-&gt;CreateGeometryShader( pGeometryShaderBuffer-&gt;GetBufferPointer(),
               pGeometryShaderBuffer-&gt;GetBufferSize(), NULL, &amp;g_pGeometryShader11 );
     
          </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

