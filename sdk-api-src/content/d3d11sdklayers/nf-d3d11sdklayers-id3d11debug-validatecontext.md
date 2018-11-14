---
UID: NF:d3d11sdklayers.ID3D11Debug.ValidateContext
title: ID3D11Debug::ValidateContext
author: windows-sdk-content
description: Check to see if the draw pipeline state is valid.
old-location: direct3d11\id3d11debug_validatecontext.htm
tech.root: direct3d11
ms.assetid: c8679a68-336f-4bfa-91d6-398a75b34dfb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 4ee713bf-94e0-0a30-fb72-d6e8a2216e88, ID3D11Debug interface [Direct3D 11],ValidateContext method, ID3D11Debug.ValidateContext, ID3D11Debug::ValidateContext, ValidateContext, ValidateContext method [Direct3D 11], ValidateContext method [Direct3D 11],ID3D11Debug interface, d3d11sdklayers/ID3D11Debug::ValidateContext, direct3d11.id3d11debug_validatecontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11sdklayers.h
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
 - ID3D11Debug.ValidateContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11sdklayers.h
: 
- ID3D11Debug.ValidateContext
: 
---

# ID3D11Debug::ValidateContext


## -description


Check to see if the draw pipeline state is valid.


## -parameters




### -param pContext [in]

Type: <b><a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>, that represents a device context.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



Use validate prior to calling a draw method (for example, <a href="https://msdn.microsoft.com/9c63067b-c7ac-412c-ad49-c35d4fba1d68">ID3D11DeviceContext::Draw</a>); validation requires the debug layer.




## -see-also




<a href="https://msdn.microsoft.com/2c640295-7a91-4a7a-92d3-909d288eb0d6">ID3D11Debug Interface</a>
 

 

