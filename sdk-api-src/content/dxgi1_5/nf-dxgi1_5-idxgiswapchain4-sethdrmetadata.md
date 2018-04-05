---
UID: NF:dxgi1_5.IDXGISwapChain4.SetHDRMetaData
title: IDXGISwapChain4::SetHDRMetaData method
author: windows-driver-content
description: This method sets High Dynamic Range (HDR) and Wide Color Gamut (WCG) header metadata.
old-location: direct3ddxgi\idxgiswapchain4_sethdrmetadata.htm
old-project: direct3ddxgi
ms.assetid: 03EBBB29-EAC3-4FE7-9CA7-D9F62CFDA8FB
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IDXGISwapChain4, IDXGISwapChain4 interface [DXGI], SetHDRMetaData method, IDXGISwapChain4::SetHDRMetaData, SetHDRMetaData method [DXGI], SetHDRMetaData method [DXGI], IDXGISwapChain4 interface, SetHDRMetaData,IDXGISwapChain4.SetHDRMetaData, direct3ddxgi.idxgiswapchain4_sethdrmetadata, dxgi1_5/IDXGISwapChain4::SetHDRMetaData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DXGI_RECLAIM_RESOURCE_RESULTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxgi1_5.dll
api_name:
-	IDXGISwapChain4.SetHDRMetaData
product: Windows
targetos: Windows
req.lib: Dxgi1_5.lib
req.dll: Dxgi1_5.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain4::SetHDRMetaData method


## -description


This method sets High Dynamic Range (HDR) and Wide Color Gamut (WCG)  header metadata.


## -parameters




### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/EFDFEB2E-8631-4BD6-ADA1-D415B70CCBCD">DXGI_HDR_METADATA_TYPE</a></b>

Specifies one member of the  <a href="https://msdn.microsoft.com/EFDFEB2E-8631-4BD6-ADA1-D415B70CCBCD">DXGI_HDR_METADATA_TYPE</a> enum.


### -param Size [in]

Type: <b>UINT</b>

Specifies the size of <i>pMetaData</i>, in bytes.


### -param pMetaData [in, optional]

Type: <b>void*</b>

Specifies a void pointer that references the metadata, if it exists. Refer to the <a href="https://msdn.microsoft.com/67A53A43-121F-4D83-AACC-D25D58123BE1">DXGI_HDR_METADATA_HDR10</a> structure.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



This method sets metadata to enable a monitor's output to be adjusted depending on its capabilities.




## -see-also




<a href="https://msdn.microsoft.com/DD7401E1-9991-48D8-AD23-4D34238EA4AF">DXGI 1.5 Improvements</a>



<a href="https://msdn.microsoft.com/F24AF5B3-AEEF-433E-A597-4A588B9B1D2B">IDXGISwapChain4</a>
 

 

