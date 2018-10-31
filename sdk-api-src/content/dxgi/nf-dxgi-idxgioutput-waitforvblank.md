---
UID: NF:dxgi.IDXGIOutput.WaitForVBlank
title: IDXGIOutput::WaitForVBlank
author: windows-sdk-content
description: Halt a thread until the next vertical blank occurs.
old-location: direct3ddxgi\idxgioutput_waitforvblank.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_waitforvblank.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 66e3ebb7-4b8b-3ceb-15fe-6d9cfdb9cb90, IDXGIOutput interface [DXGI],WaitForVBlank method, IDXGIOutput.WaitForVBlank, IDXGIOutput::WaitForVBlank, WaitForVBlank, WaitForVBlank method [DXGI], WaitForVBlank method [DXGI],IDXGIOutput interface, direct3ddxgi.idxgioutput_waitforvblank, dxgi/IDXGIOutput::WaitForVBlank
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
 - IDXGIOutput.WaitForVBlank
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIOutput::WaitForVBlank


## -description


Halt a thread until the next vertical blank occurs.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



A vertical blank occurs when the raster moves from the lower right corner to the upper left corner to begin drawing the next frame.




## -see-also




<a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a>
 

 

