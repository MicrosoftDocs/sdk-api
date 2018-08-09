---
UID: NF:d3d10effect.D3D10StateBlockMaskUnion
title: D3D10StateBlockMaskUnion function
author: windows-sdk-content
description: Combine two state-block masks with a bitwise OR.
old-location: direct3d10\d3d10stateblockmaskunion.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskunion.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10StateBlockMaskUnion, D3D10StateBlockMaskUnion function [Direct3D 10], c41aabcb-aa6c-e4b6-5de4-b68cb7241686, d3d10effect/D3D10StateBlockMaskUnion, direct3d10.d3d10stateblockmaskunion
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
 - D3D10StateBlockMaskUnion
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10StateBlockMaskUnion function


## -description


Combine two state-block masks with a bitwise OR.


## -parameters




### -param pA [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask on the left side of the bitwise OR operation. See <a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>.


### -param pB [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask on the right side of the bitwise OR operation.


### -param pResult [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>*</b>

The result of the bitwise OR operation.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205151(v=VS.85).aspx">Core Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205177(v=VS.85).aspx">Effect Functions</a>
 

 

