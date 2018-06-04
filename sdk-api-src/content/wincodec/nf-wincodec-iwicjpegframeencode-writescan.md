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

# IWICJpegFrameEncode::WriteScan


## -description


Writes scan data to a JPEG frame.


## -parameters




### -param cbScanData

Type: <b>UINT</b>

The size of the data in the <i>pbScanData</i> parameter.


### -param pbScanData

Type: <b>BYTE*</b>

The scan data to write.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK on successful completion.




## -remarks



<b>WriteScan</b> may be called multiple times.  Each call appends the scan data specified to any previous scan data.  Complete the scan by calling <a href="https://msdn.microsoft.com/6321fb9e-9ea8-423c-a332-9daa589af6f7">IWICBitmapFrameEncode::Commit</a>.



Any calls to set encoder parameters or image metadata that will appear before the scan data in the resulting JPEG file must be completed before the first call to this method.  This includes calls to <a href="https://msdn.microsoft.com/c955dede-297f-44c1-aa03-31a07a6d69d2">IWICBitmapFrameEncode::SetColorContexts</a> , <a href="https://msdn.microsoft.com/c463fc95-695d-4ba3-bf62-5b09d69c60c2">IWICBitmapFrameEncode::SetPalette</a>, <a href="https://msdn.microsoft.com/9327b5dd-18a3-40c6-8bb4-245fcc7fb582">IWICBitmapFrameEncode::SetPixelFormat</a>, <a href="https://msdn.microsoft.com/0b9e564a-5278-41d7-84ab-8b7594e776c7">IWICBitmapFrameEncode::SetResolution</a>, and <a href="https://msdn.microsoft.com/da6924cf-87c0-4774-a02e-5d54be65ef28">IWICBitmapFrameEncode::SetThumbnail</a>.  <a href="https://msdn.microsoft.com/e21e1a66-b1fa-4700-a14e-dc382b5404f7">IWICBitmapFrameEncode::SetSize</a> is required as it has no default value for encoded image size.





## -see-also




<a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a>



<a href="https://msdn.microsoft.com/631571A2-AA15-4A4B-B705-6CCC81392A6A">IWICJpegFrameEncode</a>
 

 

