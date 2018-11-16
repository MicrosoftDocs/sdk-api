---
UID: NF:d3d11.ID3D11Device.CreateDomainShader
title: ID3D11Device::CreateDomainShader
author: windows-sdk-content
description: Create a domain shader.
old-location: direct3d11\id3d11device_createdomainshader.htm
tech.root: direct3d11
ms.assetid: 414525a8-55ad-4d37-a302-5c30909588f1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 8c230b52-7c67-4576-98d9-238d464c9620, CreateDomainShader, CreateDomainShader method [Direct3D 11], CreateDomainShader method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateDomainShader method, ID3D11Device.CreateDomainShader, ID3D11Device::CreateDomainShader, d3d11/ID3D11Device::CreateDomainShader, direct3d11.id3d11device_createdomainshader
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
 - ID3D11Device.CreateDomainShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11Device.CreateDomainShader
: 
---

# ID3D11Device::CreateDomainShader


## -description


Create a <a href="https://msdn.microsoft.com/en-us/library/Ff476340(v=VS.85).aspx">domain shader</a>.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to a compiled shader.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">SIZE_T</a></b>

Size of the compiled shader.


### -param pClassLinkage [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476358(v=VS.85).aspx">ID3D11ClassLinkage</a>*</b>

A pointer to a class linkage interface (see <a href="https://msdn.microsoft.com/en-us/library/Ff476358(v=VS.85).aspx">ID3D11ClassLinkage</a>); the value can be <b>NULL</b>.


### -param ppDomainShader [out, optional]

Type: <b><a href="https://msdn.microsoft.com/cd01c872-4df5-4741-90c5-211d3e393f89">ID3D11DomainShader</a>**</b>

Address of a pointer to a <a href="https://msdn.microsoft.com/cd01c872-4df5-4741-90c5-211d3e393f89">ID3D11DomainShader</a> interface. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return <b>S_FALSE</b> instead of <b>S_OK</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -remarks



The Direct3D 11.1 runtime, which is available starting with Windows 8, provides the following new functionality for <b>CreateDomainShader</b>.

The following shader model 5.0 instructions are available to just pixel shaders and compute shaders in the Direct3D 11.0 runtime. For the Direct3D 11.1 runtime, because unordered access views (UAV) are available at all shader stages, you can use these instructions in all shader stages.

Therefore, if you use the following shader model 5.0 instructions in a domain shader, you can successfully pass the compiled domain shader to <i>pShaderBytecode</i>. That is, the call to <b>CreateDomainShader</b> succeeds.

If you pass a compiled shader to <i>pShaderBytecode</i> that uses any of the following instructions on a device that doesn’t support UAVs at every shader stage (including existing drivers that are not implemented to support UAVs at every shader stage), <b>CreateDomainShader</b> fails.  <b>CreateDomainShader</b> also fails if the shader tries to use a UAV slot beyond the set of UAV slots that the hardware supports.

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446942(v=VS.85).aspx">dcl_uav_typed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446938(v=VS.85).aspx">dcl_uav_raw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446941(v=VS.85).aspx">dcl_uav_structured</a>
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
 

 

