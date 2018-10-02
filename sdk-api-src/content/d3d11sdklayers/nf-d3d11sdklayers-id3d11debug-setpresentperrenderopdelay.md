---
UID: NF:d3d11sdklayers.ID3D11Debug.SetPresentPerRenderOpDelay
title: ID3D11Debug::SetPresentPerRenderOpDelay
author: windows-sdk-content
description: Set the number of milliseconds to sleep after IDXGISwapChain::Present is called.
old-location: direct3d11\id3d11debug_setpresentperrenderopdelay.htm
tech.root: direct3d11
ms.assetid: 72489871-819a-4f75-a3ad-03f93f5c7761
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 573cbcb7-dbec-80ce-3edb-e1d60b5c1261, ID3D11Debug interface [Direct3D 11],SetPresentPerRenderOpDelay method, ID3D11Debug.SetPresentPerRenderOpDelay, ID3D11Debug::SetPresentPerRenderOpDelay, SetPresentPerRenderOpDelay, SetPresentPerRenderOpDelay method [Direct3D 11], SetPresentPerRenderOpDelay method [Direct3D 11],ID3D11Debug interface, d3d11sdklayers/ID3D11Debug::SetPresentPerRenderOpDelay, direct3d11.id3d11debug_setpresentperrenderopdelay
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
 - ID3D11Debug.SetPresentPerRenderOpDelay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Debug::SetPresentPerRenderOpDelay


## -description


Set the number of milliseconds to sleep after <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a> is called.


## -parameters




### -param Milliseconds

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of milliseconds to sleep after Present is called.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The application will only sleep if D3D11_DEBUG_FEATURE_PRESENT_PER_RENDER_OP is a set in the <a href="https://msdn.microsoft.com/60f9da61-dc97-4b6d-b187-df3605ad9336">feature mask</a>. If that flag is not set the number of milliseconds is set but ignored and the application does not sleep. 10ms is used as a default value if this method is never called.




## -see-also




<a href="https://msdn.microsoft.com/2c640295-7a91-4a7a-92d3-909d288eb0d6">ID3D11Debug Interface</a>
 

 

