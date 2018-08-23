---
UID: NF:d3d10effect.D3D10CreateStateBlock
title: D3D10CreateStateBlock function
author: windows-sdk-content
description: Create a state block.
old-location: direct3d10\d3d10createstateblock.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createstateblock.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 8f57946f-10b9-397f-8aa5-63df2e9ef7df, D3D10CreateStateBlock, D3D10CreateStateBlock function [Direct3D 10], d3d10effect/D3D10CreateStateBlock, direct3d10.d3d10createstateblock
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
 - D3D10CreateStateBlock
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10CreateStateBlock function


## -description


Create a state block.


## -parameters




### -param pDevice [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>*</b>

The device for which the state block will be created.


### -param pStateBlockMask [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>*</b>

Indicates which parts of the device state will be captured when calling <a href="https://msdn.microsoft.com/en-us/library/Bb173858(v=VS.85).aspx">ID3D10StateBlock::Capture</a> and reapplied when calling <a href="https://msdn.microsoft.com/en-us/library/Bb173857(v=VS.85).aspx">ID3D10StateBlock::Apply</a>. See remarks.


### -param ppStateBlock [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173856(v=VS.85).aspx">ID3D10StateBlock</a>**</b>

Address of a pointer to the buffer created (see <a href="https://msdn.microsoft.com/en-us/library/Bb173856(v=VS.85).aspx">ID3D10StateBlock Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



A state block is a collection of device state, and is used for saving and restoring device state. Use a state-block mask to enable subsets of state for saving and restoring.

The <a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a> structure can be filled manually or by using any of the D3D10StateBlockMaskXXX APIs. A state block mask can also be obtained by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173709(v=VS.85).aspx">ID3D10EffectTechnique::ComputeStateBlockMask</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb173658(v=VS.85).aspx">ID3D10EffectPass::ComputeStateBlockMask</a>.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

In Direct3D 10, a state block object does not contain any valid information about the state of the device until <a href="https://msdn.microsoft.com/en-us/library/Bb173858(v=VS.85).aspx">ID3D10StateBlock::Capture</a> is called. In Direct3D 9, state is saved in a state block object, when it is created.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205151(v=VS.85).aspx">Core Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205177(v=VS.85).aspx">Effect Functions</a>
 

 

