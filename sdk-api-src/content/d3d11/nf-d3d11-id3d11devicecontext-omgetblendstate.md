---
UID: NF:d3d11.ID3D11DeviceContext.OMGetBlendState
title: ID3D11DeviceContext::OMGetBlendState
author: windows-sdk-content
description: Get the blend state of the output-merger stage.
old-location: direct3d11\id3d11devicecontext_omgetblendstate.htm
old-project: direct3d11
ms.assetid: 871429b4-8f4a-43bb-ae55-3b07f8d00f68
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],OMGetBlendState method, ID3D11DeviceContext.OMGetBlendState, ID3D11DeviceContext::OMGetBlendState, OMGetBlendState, OMGetBlendState method [Direct3D 11], OMGetBlendState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMGetBlendState, db30eb26-ca10-d827-172b-7c7a6fe1ff83, direct3d11.id3d11devicecontext_omgetblendstate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.OMGetBlendState
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::OMGetBlendState


## -description


Get the blend state of the output-merger stage.


## -parameters




### -param ppBlendState [out, optional]

Type: <b><a href="https://msdn.microsoft.com/ccb39c89-eba7-473c-8358-dc3513da4be7">ID3D11BlendState</a>**</b>

Address of a pointer to a blend-state interface (see <a href="https://msdn.microsoft.com/ccb39c89-eba7-473c-8358-dc3513da4be7">ID3D11BlendState</a>).
          


### -param BlendFactor [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a>[4]</b>

Array of blend factors, one for each RGBA component.


### -param pSampleMask [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/fabcae1d-2ad8-4f4d-8eef-18945e369225">sample mask</a>.
          


## -returns



Returns nothing.




## -remarks



The reference count of the returned interface will be incremented by one when the blend state is retrieved. Applications must release returned pointer(s) when they are no longer needed, or else there will be a memory leak.

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

