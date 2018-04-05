---
UID: NE:d3d11.D3D11_CLEAR_FLAG
title: D3D11_CLEAR_FLAG
author: windows-driver-content
description: Specifies the parts of the depth stencil to clear.
old-location: direct3d11\d3d11_clear_flag.htm
old-project: direct3d11
ms.assetid: 6da515f3-d71d-4b59-b2ea-cacdf78fcb42
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 88ebcd50-b0dd-e04e-4b30-028ca4147553, D3D11_CLEAR_DEPTH, D3D11_CLEAR_FLAG, D3D11_CLEAR_FLAG enumeration [Direct3D 11], D3D11_CLEAR_STENCIL, d3d11/D3D11_CLEAR_DEPTH, d3d11/D3D11_CLEAR_FLAG, d3d11/D3D11_CLEAR_STENCIL, direct3d11.d3d11_clear_flag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3D11_CLEAR_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11.h
api_name:
-	D3D11_CLEAR_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_CLEAR_FLAG enumeration


## -description



      Specifies the parts of the depth stencil to clear.


## -enum-fields




### -field D3D11_CLEAR_DEPTH

Clear the depth buffer, using fast clear if possible, then place the resource in a compressed state.


### -field D3D11_CLEAR_STENCIL

Clear the stencil buffer, using fast clear if possible, then place the resource in a compressed state.


## -remarks




          These flags are used when calling <a href="https://msdn.microsoft.com/1e2269cf-edef-466e-be59-95dc644c7a0c">ID3D11DeviceContext::ClearDepthStencilView</a>; the flags can be combined with a bitwise OR.
        




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

