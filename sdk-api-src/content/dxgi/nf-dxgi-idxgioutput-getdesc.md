---
UID: NF:dxgi.IDXGIOutput.GetDesc
title: IDXGIOutput::GetDesc (dxgi.h)
author: windows-sdk-content
description: Get a description of the output.
old-location: direct3ddxgi\idxgioutput_getdesc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getdesc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 895d1ca4-22a2-332a-34a7-b0c55200b423, GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetDesc method, IDXGIOutput.GetDesc, IDXGIOutput::GetDesc, direct3ddxgi.idxgioutput_getdesc, dxgi/IDXGIOutput::GetDesc
ms.topic: method
f1_keywords: 
 - "dxgi/IDXGIOutput.GetDesc"
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
 - IDXGIOutput.GetDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIOutput::GetDesc


## -description


Get a description of the output.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dxgi/ns-dxgi-dxgi_output_desc">DXGI_OUTPUT_DESC</a>*</b>

A pointer to the output description (see <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/ns-dxgi-dxgi_output_desc">DXGI_OUTPUT_DESC</a>).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns a code that indicates success or failure. S_OK if successful, <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a> if <i>pDesc</i> is passed in as <b>NULL</b>.




## -remarks



 On a high DPI desktop, <b>GetDesc</b> returns the visualized screen size unless the app is marked high DPI aware. For info about writing DPI-aware Win32 apps, see <a href="https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>
 

 

