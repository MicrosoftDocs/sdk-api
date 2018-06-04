---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDXGISwapChain4::SetHDRMetaData


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
 

 

