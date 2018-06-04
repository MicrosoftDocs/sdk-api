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

# IDXGIFactory5::CheckFeatureSupport


## -description


Used to check for hardware feature support.


## -parameters




### -param Feature

Type: <b><a href="https://msdn.microsoft.com/207D5BDC-5D10-4F84-931F-4812574FA74B">DXGI_FEATURE</a></b>

Specifies one member of  <a href="https://msdn.microsoft.com/207D5BDC-5D10-4F84-931F-4812574FA74B">DXGI_FEATURE</a> to query support for.


### -param pFeatureSupportData [in, out]

Type: <b>void*</b>

Specifies a pointer to a buffer that will be filled with data that describes the feature support.


### -param FeatureSupportDataSize

Type: <b>UINT</b>

The size, in bytes, of <i>pFeatureSupportData</i>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



Refer to the description of <a href="https://msdn.microsoft.com/c0030570-89ba-4586-a358-8c3b8c393a90">DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</a>.




## -see-also




<a href="https://msdn.microsoft.com/DB77E4DE-62FF-4AA3-BDA9-847ABB38973B">IDXGIFactory5</a>
 

 

