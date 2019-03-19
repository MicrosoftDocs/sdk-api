---
UID: NF:d3d11sdklayers.ID3D11Debug.ValidateContextForDispatch
title: ID3D11Debug::ValidateContextForDispatch (d3d11sdklayers.h)
author: windows-sdk-content
description: Verifies whether the dispatch pipeline state is valid.
old-location: direct3d11\id3d11debug_validatecontextfordispatch.htm
tech.root: direct3d11
ms.assetid: 0ddabb4f-eeed-46d4-a1d2-501180edffe0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11Debug interface [Direct3D 11],ValidateContextForDispatch method, ID3D11Debug.ValidateContextForDispatch, ID3D11Debug::ValidateContextForDispatch, ValidateContextForDispatch, ValidateContextForDispatch method [Direct3D 11], ValidateContextForDispatch method [Direct3D 11],ID3D11Debug interface, d3d11sdklayers/ID3D11Debug::ValidateContextForDispatch, direct3d11.id3d11debug_validatecontextfordispatch
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
 - ID3D11Debug.ValidateContextForDispatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Debug::ValidateContextForDispatch


## -description


Verifies whether the dispatch pipeline state is valid.


## -parameters




### -param pContext [in]

Type: <b><a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> that represents a device context.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the return codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



Use this method before you call a dispatch method (for example, <a href="https://msdn.microsoft.com/7d3401bb-521f-4ab0-8833-e5caf712d0c9">ID3D11DeviceContext::Dispatch</a>). Validation requires the debug layer.




## -see-also




<a href="https://msdn.microsoft.com/2c640295-7a91-4a7a-92d3-909d288eb0d6">ID3D11Debug</a>
 

 

