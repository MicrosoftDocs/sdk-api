---
UID: NF:d3d10effect.D3D10StateBlockMaskIntersect
title: D3D10StateBlockMaskIntersect function (d3d10effect.h)
author: windows-sdk-content
description: Combine two state-block masks with a bitwise AND.
old-location: direct3d10\d3d10stateblockmaskintersect.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskintersect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 7ef37c3a-8924-5736-9b40-6a56cdf480c7, D3D10StateBlockMaskIntersect, D3D10StateBlockMaskIntersect function [Direct3D 10], d3d10effect/D3D10StateBlockMaskIntersect, direct3d10.d3d10stateblockmaskintersect
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
 - D3D10StateBlockMaskIntersect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# D3D10StateBlockMaskIntersect function


## -description


Combine two state-block masks with a bitwise AND.


## -parameters




### -param pA [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask on the left side of the bitwise AND operation. See <a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>.


### -param pB [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask on the right side of the bitwise AND operation.


### -param pResult [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>*</b>

The result of the bitwise AND operation.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205151(v=VS.85).aspx">Core Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205177(v=VS.85).aspx">Effect Functions</a>
 

 

