---
UID: NF:dxgi.IDXGIOutput.GetFrameStatistics
title: IDXGIOutput::GetFrameStatistics
author: windows-sdk-content
description: Gets statistics about recently rendered frames.
old-location: direct3ddxgi\idxgioutput_getframestatistics.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getframestatistics.htm
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: 2986a9cc-4b09-8622-8d30-17f06409df3a, GetFrameStatistics, GetFrameStatistics method [DXGI], GetFrameStatistics method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetFrameStatistics method, IDXGIOutput.GetFrameStatistics, IDXGIOutput::GetFrameStatistics, direct3ddxgi.idxgioutput_getframestatistics, dxgi/IDXGIOutput::GetFrameStatistics
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgi.h
: 
- IDXGIOutput.GetFrameStatistics
: 
---

# IDXGIOutput::GetFrameStatistics


## -description


Gets statistics about recently rendered frames.


## -parameters




### -param pStats [out]

Type: <b><a href="https://msdn.microsoft.com/183232b9-9a08-4356-afcd-92078450ced8">DXGI_FRAME_STATISTICS</a>*</b>

A pointer to frame statistics (see <a href="https://msdn.microsoft.com/183232b9-9a08-4356-afcd-92078450ced8">DXGI_FRAME_STATISTICS</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this function succeeds, it returns S_OK. Otherwise, it might return <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a>.




## -remarks



This API is similar to <a href="https://msdn.microsoft.com/c02b9e3b-5d59-4ed2-b373-2097c0e46f70">IDXGISwapChain::GetFrameStatistics</a>.


<div class="alert"><b>Note</b>  Calling this method is only supported while in full-screen mode.</div>
<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a>
 

 

