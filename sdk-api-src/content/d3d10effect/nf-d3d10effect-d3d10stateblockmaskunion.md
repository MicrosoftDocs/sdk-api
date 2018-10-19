---
UID: NF:d3d10effect.D3D10StateBlockMaskUnion
title: D3D10StateBlockMaskUnion function
author: windows-sdk-content
description: Combine two state-block masks with a bitwise OR.
old-location: direct3d10\d3d10stateblockmaskunion.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskunion.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D10StateBlockMaskUnion, D3D10StateBlockMaskUnion function [Direct3D 10], c41aabcb-aa6c-e4b6-5de4-b68cb7241686, d3d10effect/D3D10StateBlockMaskUnion, direct3d10.d3d10stateblockmaskunion
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
 - D3D10StateBlockMaskUnion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D10StateBlockMaskUnion function


## -description


Combine two state-block masks with a bitwise OR.


## -parameters




### -param pA [in]

Type: <b><a href="https://msdn.microsoft.com/3188002c-a49f-4991-8fd5-75b31de8b790">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask on the left side of the bitwise OR operation. See <a href="https://msdn.microsoft.com/3188002c-a49f-4991-8fd5-75b31de8b790">D3D10_STATE_BLOCK_MASK</a>.


### -param pB [in]

Type: <b><a href="https://msdn.microsoft.com/3188002c-a49f-4991-8fd5-75b31de8b790">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask on the right side of the bitwise OR operation.


### -param pResult [out]

Type: <b><a href="https://msdn.microsoft.com/3188002c-a49f-4991-8fd5-75b31de8b790">D3D10_STATE_BLOCK_MASK</a>*</b>

The result of the bitwise OR operation.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/012577cd-970e-43bc-996e-3be7c2283b60">Core Functions</a>



<a href="https://msdn.microsoft.com/b76643f0-387f-49c6-80e5-4d7b406b4db7">Effect Functions</a>
 

 

