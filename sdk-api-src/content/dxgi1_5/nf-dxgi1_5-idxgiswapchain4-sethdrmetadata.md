---
UID: NF:dxgi1_5.IDXGISwapChain4.SetHDRMetaData
title: IDXGISwapChain4::SetHDRMetaData (dxgi1_5.h)
author: windows-sdk-content
description: This method sets High Dynamic Range (HDR) and Wide Color Gamut (WCG) header metadata.
old-location: direct3ddxgi\idxgiswapchain4_sethdrmetadata.htm
tech.root: direct3ddxgi
ms.assetid: 03EBBB29-EAC3-4FE7-9CA7-D9F62CFDA8FB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain4 interface [DXGI],SetHDRMetaData method, IDXGISwapChain4.SetHDRMetaData, IDXGISwapChain4::SetHDRMetaData, SetHDRMetaData, SetHDRMetaData method [DXGI], SetHDRMetaData method [DXGI],IDXGISwapChain4 interface, direct3ddxgi.idxgiswapchain4_sethdrmetadata, dxgi1_5/IDXGISwapChain4::SetHDRMetaData
ms.topic: method
f1_keywords: ["dxgi1_5/IDXGISwapChain4.SetHDRMetaData"]
req.header: dxgi1_5.h
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
req.lib: Dxgi1_5.lib
req.dll: Dxgi1_5.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi1_5.dll
api_name:
 - IDXGISwapChain4.SetHDRMetaData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGISwapChain4::SetHDRMetaData


## -description


This method sets High Dynamic Range (HDR) and Wide Color Gamut (WCG)  header metadata.


## -parameters




### -param Type [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type">DXGI_HDR_METADATA_TYPE</a></b>

Specifies one member of the  <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type">DXGI_HDR_METADATA_TYPE</a> enum.


### -param Size [in]

Type: <b>UINT</b>

Specifies the size of <i>pMetaData</i>, in bytes.


### -param pMetaData [in, optional]

Type: <b>void*</b>

Specifies a void pointer that references the metadata, if it exists. Refer to the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/ns-dxgi1_5-dxgi_hdr_metadata_hdr10">DXGI_HDR_METADATA_HDR10</a> structure.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



This method sets metadata to enable a monitor's output to be adjusted depending on its capabilities.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-1-5-improvements">DXGI 1.5 Improvements</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nn-dxgi1_5-idxgiswapchain4">IDXGISwapChain4</a>
 

 

