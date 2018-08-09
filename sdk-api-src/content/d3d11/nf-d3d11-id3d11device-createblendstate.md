---
UID: NF:d3d11.ID3D11Device.CreateBlendState
title: ID3D11Device::CreateBlendState
author: windows-sdk-content
description: Create a blend-state object that encapsules blend state for the output-merger stage.
old-location: direct3d11\id3d11device_createblendstate.htm
old-project: direct3d11
ms.assetid: 05b27d72-6ae5-4bab-8906-2d1373ea8d4c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 3e6800b8-cd67-743c-c74d-b23a9a29daea, CreateBlendState, CreateBlendState method [Direct3D 11], CreateBlendState method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateBlendState method, ID3D11Device.CreateBlendState, ID3D11Device::CreateBlendState, d3d11/ID3D11Device::CreateBlendState, direct3d11.id3d11device_createblendstate
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
 - ID3D11Device.CreateBlendState
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CreateBlendState


## -description


Create a blend-state object that encapsules blend state for the output-merger stage.


## -parameters




### -param pBlendStateDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/388f862c-58b0-48a8-a865-ba7568484ef5">D3D11_BLEND_DESC</a>*</b>

Pointer to a blend-state description (see <a href="https://msdn.microsoft.com/388f862c-58b0-48a8-a865-ba7568484ef5">D3D11_BLEND_DESC</a>).
          


### -param ppBlendState [out, optional]

Type: <b><a href="https://msdn.microsoft.com/ccb39c89-eba7-473c-8358-dc3513da4be7">ID3D11BlendState</a>**</b>

Address of a pointer to the blend-state object created (see <a href="https://msdn.microsoft.com/ccb39c89-eba7-473c-8358-dc3513da4be7">ID3D11BlendState</a>).
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the blend-state object.
              See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for other possible return values.
            




## -remarks



An application can create up to 4096 unique blend-state objects. For each object created, the runtime checks to see if a previous object
          has the same state. If such a previous object exists, the runtime will return a pointer to previous instance instead of creating a duplicate object.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

