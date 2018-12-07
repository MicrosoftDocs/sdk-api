---
UID: NF:d3d10effect.D3D10CreateEffectFromMemory
title: D3D10CreateEffectFromMemory function
author: windows-sdk-content
description: Creates an ID3D10Effect from a buffer containing a compiled effect.
old-location: direct3d10\d3d10createeffectfrommemory.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createeffectfrommemory.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D10CreateEffectFromMemory, D3D10CreateEffectFromMemory function [Direct3D 10], d3d10effect/D3D10CreateEffectFromMemory, direct3d10.d3d10createeffectfrommemory, f306b99a-20d9-c501-65b4-81dd11930f56
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d3d10effect.h
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10CreateEffectFromMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D10CreateEffectFromMemory function


## -description


Creates an ID3D10Effect from a buffer containing a compiled effect.


## -parameters




### -param pData [in]

Type: <b>void*</b>

A pointer to a compiled effect.


### -param DataLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of <i>pData</i>.


### -param FXFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Effect <a href="https://msdn.microsoft.com/434bcff8-47ea-480d-bc0b-44d3ed1f8cce">compile options</a>.


### -param pDevice [in]

Type: <b><a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>*</b>

A pointer to the device (see <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>).


### -param pEffectPool [in]

Type: <b><a href="https://msdn.microsoft.com/e64c9285-f4ee-4bed-a57d-8ccc3e6b3ba3">ID3D10EffectPool</a>*</b>

Optional. A pointer to an memory space for effect variables that are shared across effects (see <a href="https://msdn.microsoft.com/e64c9285-f4ee-4bed-a57d-8ccc3e6b3ba3">ID3D10EffectPool Interface</a>).


### -param ppEffect [out]

Type: <b><a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect</a>**</b>

A pointer to an <a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect Interface</a> which contains the created effect.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



This method is used to create an <a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect Interface</a> object from an effect that has been compiled before runtime and loaded into memory.  
      For help precompiling an effect, see <a href="https://msdn.microsoft.com/56806335-a0c7-4247-b40d-ba93486a88ac">Offline Compiling</a>.  
      To load and compile an ASCII .fx file see <a href="https://msdn.microsoft.com/b8d8a0b7-b520-44e4-8691-6eb46202c092">Compile an Effect (Direct3D 10)</a>.


#### Examples

Compiling and loading an effect
          

Compile the effect.


```

fxc.exe /T fx_4_0 /Fo Tutorial03.fxo Tutorial03.fx      
          
```


Load the compiled effect at runtime.


```

ifstream is("tutorial03.fxo", ios::binary);
is.seekg(0,ios_base::end);
streampos pos = is.tellg();
is.seekg(0,ios_base::beg);
char * effectBuffer = new char[pos];
is.read(effectBuffer,pos);
	
hr = D3D10CreateEffectFromMemory((void *)effectBuffer,pos,0,g_pd3dDevice,NULL,&g_pEffect);
          
```


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b76643f0-387f-49c6-80e5-4d7b406b4db7">Effect Functions (Direct3D 10)</a>
 

 

