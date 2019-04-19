---
UID: NF:d3d11.ID3D11DeviceContext.RSSetState
title: ID3D11DeviceContext::RSSetState (d3d11.h)
author: windows-sdk-content
description: Set the rasterizer state for the rasterizer stage of the pipeline.
old-location: direct3d11\id3d11devicecontext_rssetstate.htm
tech.root: direct3d11
ms.assetid: aa76cd3f-5d08-48e7-bd38-ff4d7119eae3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6a517464-81db-3af7-335a-c1eefddd9385, ID3D11DeviceContext interface [Direct3D 11],RSSetState method, ID3D11DeviceContext.RSSetState, ID3D11DeviceContext::RSSetState, RSSetState, RSSetState method [Direct3D 11], RSSetState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::RSSetState, direct3d11.id3d11devicecontext_rssetstate
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
 - ID3D11DeviceContext.RSSetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11DeviceContext::RSSetState


## -description


Set the <a href="https://msdn.microsoft.com/53252fef-f557-46d1-b6a7-ccc8a059752a">rasterizer state</a> for the rasterizer stage of the pipeline.


## -parameters




### -param pRasterizerState [in, optional]

Type: <b><a href="https://msdn.microsoft.com/fbe6d2b9-375e-4390-9d34-36acef0a5aa2">ID3D11RasterizerState</a>*</b>

Pointer to a rasterizer-state interface (see <a href="https://msdn.microsoft.com/fbe6d2b9-375e-4390-9d34-36acef0a5aa2">ID3D11RasterizerState</a>) to bind to the pipeline.


## -returns



Returns nothing.




## -remarks



To create a rasterizer state interface, call <a href="https://msdn.microsoft.com/b49a8dbb-2280-4d5d-ae65-58cde2e9ed10">ID3D11Device::CreateRasterizerState</a>.

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

