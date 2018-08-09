---
UID: NF:d3d10effect.D3D10StateBlockMaskDisableCapture
title: D3D10StateBlockMaskDisableCapture function
author: windows-sdk-content
description: Disable state capturing with a state-block mask.
old-location: direct3d10\d3d10stateblockmaskdisablecapture.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskdisablecapture.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 94486a35-b1e6-78b2-b9fb-00c0ab5d19f3, D3D10StateBlockMaskDisableCapture, D3D10StateBlockMaskDisableCapture function [Direct3D 10], d3d10effect/D3D10StateBlockMaskDisableCapture, direct3d10.d3d10stateblockmaskdisablecapture
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D10StateBlockMaskDisableCapture
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10StateBlockMaskDisableCapture function


## -description


Disable state capturing with a state-block mask.


## -parameters




### -param pMask [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>*</b>

A state block mask (see <a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>).


### -param StateType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205039(v=VS.85).aspx">D3D10_DEVICE_STATE_TYPES</a></b>

The type of device state to disable (see <a href="https://msdn.microsoft.com/en-us/library/Bb205039(v=VS.85).aspx">D3D10_DEVICE_STATE_TYPES</a>).


### -param RangeStart [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The lower end of the range of values to set to false.


### -param RangeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The upper end of the range of values to set to false.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This is an example of how to call this function. It creates a mask that cannot capture and apply to geometry-shader samplers in slots 2 ~ 23.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
D3D10_STATE_BLOCK_MASK stateBlockMask;
D3D10StateBlockMaskDisableCapture(&amp;stateBlockMask, 
                                 D3D10_DST_GS_SAMPLERS, 
                                 2, 23);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205151(v=VS.85).aspx">Core Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205177(v=VS.85).aspx">Effect Functions</a>
 

 

