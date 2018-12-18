---
UID: NF:d3d11sdklayers.ID3D11Debug.GetPresentPerRenderOpDelay
title: ID3D11Debug::GetPresentPerRenderOpDelay
author: windows-sdk-content
description: Get the number of milliseconds to sleep after IDXGISwapChain::Present is called.
old-location: direct3d11\id3d11debug_getpresentperrenderopdelay.htm
tech.root: direct3d11
ms.assetid: 7c55f370-df9c-40d5-97d8-6e25cb9e5579
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPresentPerRenderOpDelay, GetPresentPerRenderOpDelay method [Direct3D 11], GetPresentPerRenderOpDelay method [Direct3D 11],ID3D11Debug interface, ID3D11Debug interface [Direct3D 11],GetPresentPerRenderOpDelay method, ID3D11Debug.GetPresentPerRenderOpDelay, ID3D11Debug::GetPresentPerRenderOpDelay, d3d11sdklayers/ID3D11Debug::GetPresentPerRenderOpDelay, d80fb328-cbcf-b755-35cd-3ac7f39aeff8, direct3d11.id3d11debug_getpresentperrenderopdelay
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
 - ID3D11Debug.GetPresentPerRenderOpDelay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Debug::GetPresentPerRenderOpDelay


## -description


Get the number of milliseconds to sleep after <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a> is called.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of milliseconds to sleep after Present is called.




## -remarks



Value is set with <a href="https://msdn.microsoft.com/72489871-819a-4f75-a3ad-03f93f5c7761">ID3D11Debug::SetPresentPerRenderOpDelay</a>.




## -see-also




<a href="https://msdn.microsoft.com/2c640295-7a91-4a7a-92d3-909d288eb0d6">ID3D11Debug Interface</a>
 

 

