---
UID: NF:d3d10effect.D3D10CreateEffectFromMemory
title: D3D10CreateEffectFromMemory function
author: windows-sdk-content
description: Creates an ID3D10Effect from a buffer containing a compiled effect.
old-location: direct3d10\d3d10createeffectfrommemory.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createeffectfrommemory.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: D3D10CreateEffectFromMemory, D3D10CreateEffectFromMemory function [Direct3D 10], d3d10effect/D3D10CreateEffectFromMemory, direct3d10.d3d10createeffectfrommemory, f306b99a-20d9-c501-65b4-81dd11930f56
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3d10effect.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_DEVICE_STATE_TYPES
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
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

Effect <a href="https://msdn.microsoft.com/en-us/library/Bb205176(v=VS.85).aspx">compile options</a>.


### -param pDevice [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>*</b>

A pointer to the device (see <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>).


### -param pEffectPool [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173667(v=VS.85).aspx">ID3D10EffectPool</a>*</b>

Optional. A pointer to an memory space for effect variables that are shared across effects (see <a href="https://msdn.microsoft.com/en-us/library/Bb173667(v=VS.85).aspx">ID3D10EffectPool Interface</a>).


### -param ppEffect [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect</a>**</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect Interface</a> which contains the created effect.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This method is used to create an <a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect Interface</a> object from an effect that has been compiled before runtime and loaded into memory.  
      For help precompiling an effect, see <a href="https://msdn.microsoft.com/en-us/library/Bb509710(v=VS.85).aspx">Offline Compiling</a>.  
      To load and compile an ASCII .fx file see <a href="https://msdn.microsoft.com/en-us/library/Bb205078(v=VS.85).aspx">Compile an Effect (Direct3D 10)</a>.


#### Examples

Compiling and loading an effect
          

Compile the effect.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
fxc.exe /T fx_4_0 /Fo Tutorial03.fxo Tutorial03.fx      
          </pre>
</td>
</tr>
</table></span></div>
Load the compiled effect at runtime.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
ifstream is("tutorial03.fxo", ios::binary);
is.seekg(0,ios_base::end);
streampos pos = is.tellg();
is.seekg(0,ios_base::beg);
char * effectBuffer = new char[pos];
is.read(effectBuffer,pos);
	
hr = D3D10CreateEffectFromMemory((void *)effectBuffer,pos,0,g_pd3dDevice,NULL,&amp;g_pEffect);
          </pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205177(v=VS.85).aspx">Effect Functions (Direct3D 10)</a>
 

 

