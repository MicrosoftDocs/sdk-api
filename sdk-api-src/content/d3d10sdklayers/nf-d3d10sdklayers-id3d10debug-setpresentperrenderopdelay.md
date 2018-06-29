---
UID: NF:d3d10sdklayers.ID3D10Debug.SetPresentPerRenderOpDelay
title: ID3D10Debug::SetPresentPerRenderOpDelay
author: windows-sdk-content
description: Set the number of milliseconds to sleep after Present is called.
old-location: direct3d10\id3d10debug_setpresentperrenderopdelay.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_setpresentperrenderopdelay.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 42cc51c9-dccb-4b3d-9dcc-643abb49543f, ID3D10Debug interface [Direct3D 10],SetPresentPerRenderOpDelay method, ID3D10Debug.SetPresentPerRenderOpDelay, ID3D10Debug::SetPresentPerRenderOpDelay, SetPresentPerRenderOpDelay, SetPresentPerRenderOpDelay method [Direct3D 10], SetPresentPerRenderOpDelay method [Direct3D 10],ID3D10Debug interface, d3d10sdklayers/ID3D10Debug::SetPresentPerRenderOpDelay, direct3d10.id3d10debug_setpresentperrenderopdelay
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10sdklayers.h
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
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10Debug.SetPresentPerRenderOpDelay
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Debug::SetPresentPerRenderOpDelay


## -description


Set the number of milliseconds to sleep after <a href="https://msdn.microsoft.com/library/Bb174576(v=VS.85).aspx">Present</a> is called.


## -parameters




### -param Milliseconds [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of milliseconds to sleep after Present is called.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The application will only sleep if D3D10_DEBUG_FEATURE_PRESENT_PER_RENDER_OP is a set in the <a href="https://msdn.microsoft.com/library/Bb173520(v=VS.85).aspx">feature mask</a>. If that flag is not set the number of milliseconds is set but ignored and the application does not sleep. 10ms is used as a default value if this method is never called.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173516(v=VS.85).aspx">ID3D10Debug Interface</a>
 

 

