---
UID: NF:d3d10effect.D3D10StateBlockMaskEnableCapture
title: D3D10StateBlockMaskEnableCapture function
author: windows-sdk-content
description: Enable a range of state values in a state block mask.
old-location: direct3d10\d3d10stateblockmaskenablecapture.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskenablecapture.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D10StateBlockMaskEnableCapture, D3D10StateBlockMaskEnableCapture function [Direct3D 10], d3d10effect/D3D10StateBlockMaskEnableCapture, direct3d10.d3d10stateblockmaskenablecapture, facce8d7-c03d-439b-89fb-733b2d013965
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
 - D3D10StateBlockMaskEnableCapture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D10StateBlockMaskEnableCapture function


## -description


Enable a range of state values in a state block mask.


## -parameters




### -param pMask [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>*</b>

A state block mask (see <a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>).


### -param StateType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205039(v=VS.85).aspx">D3D10_DEVICE_STATE_TYPES</a></b>

The type of device state to enable (see <a href="https://msdn.microsoft.com/en-us/library/Bb205039(v=VS.85).aspx">D3D10_DEVICE_STATE_TYPES</a>.


### -param RangeStart [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The lower end of the range of values to set to true.


### -param RangeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The upper end of the range of values to set to true.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This is an example of how to call this function. It create a mask that can capture and apply to geometry-shader samplers in slots 2 ~ 13.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
D3D10_STATE_BLOCK_MASK stateBlockMask;
D3D10StateBlockMaskEnableCapture(&amp;stateBlockMask, 
                                 D3D10_DST_GS_SAMPLERS, 
                                 2, 13);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205151(v=VS.85).aspx">Core Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205177(v=VS.85).aspx">Effect Functions</a>
 

 

