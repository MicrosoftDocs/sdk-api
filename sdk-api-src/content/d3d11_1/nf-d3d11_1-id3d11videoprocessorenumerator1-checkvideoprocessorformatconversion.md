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

# ID3D11VideoProcessorEnumerator1::CheckVideoProcessorFormatConversion


## -description


Indicates whether the driver supports the specified combination of format and colorspace conversions.


## -parameters




### -param InputFormat [in]

Type: <b>DXGI_FORMAT</b>

The format of the video processor input.


### -param InputColorSpace [in]

Type: <b>DXGI_COLOR_SPACE_TYPE</b>

The colorspace of the video processor input.


### -param OutputFormat [in]

Type: <b>DXGI_FORMAT</b>

The format of the video processor output.


### -param OutputColorSpace [in]

Type: <b>DXGI_COLOR_SPACE_TYPE</b>

The colorspace of the video processor output.


### -param pSupported [out]

Type: <b>BOOL*</b>

Pointer to a boolean that is set by the driver to indicate if the specified combination of format and colorspace conversions is supported. True if the conversion is supported; otherwise, false.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following error codes.

<table>
<tr>
<td>S_OK</td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed or this function was called using an invalid calling pattern.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/BBC4C5BC-2DA0-48BD-B182-FBF62A2491A7">ID3D11VideoProcessorEnumerator1</a>
 

 

