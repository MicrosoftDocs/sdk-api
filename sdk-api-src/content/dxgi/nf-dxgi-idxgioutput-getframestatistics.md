---
UID: NF:dxgi.IDXGIOutput.GetFrameStatistics
title: IDXGIOutput::GetFrameStatistics
author: windows-sdk-content
description: Gets statistics about recently rendered frames.
old-location: direct3ddxgi\idxgioutput_getframestatistics.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getframestatistics.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: 2986a9cc-4b09-8622-8d30-17f06409df3a, GetFrameStatistics, GetFrameStatistics method [DXGI], GetFrameStatistics method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetFrameStatistics method, IDXGIOutput.GetFrameStatistics, IDXGIOutput::GetFrameStatistics, direct3ddxgi.idxgioutput_getframestatistics, dxgi/IDXGIOutput::GetFrameStatistics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
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
req.typenames: DXGI_SWAP_EFFECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIOutput.GetFrameStatistics
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput::GetFrameStatistics


## -description


Gets statistics about recently rendered frames.


## -parameters




### -param pStats [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173060(v=VS.85).aspx">DXGI_FRAME_STATISTICS</a>*</b>

A pointer to frame statistics (see <a href="https://msdn.microsoft.com/en-us/library/Bb173060(v=VS.85).aspx">DXGI_FRAME_STATISTICS</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this function succeeds, it returns S_OK. Otherwise, it might return <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_INVALID_CALL</a>.




## -remarks



This API is similar to <a href="https://msdn.microsoft.com/en-us/library/Bb174573(v=VS.85).aspx">IDXGISwapChain::GetFrameStatistics</a>.


<div class="alert"><b>Note</b>  Calling this method is only supported while in full-screen mode.</div>
<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>
 

 

