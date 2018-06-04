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

# D3DX11_FFT_DESC structure


## -description



      Describes an FFT.


## -struct-fields




### -field NumDimensions

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Number of dimension in the FFT.
          


### -field ElementLengths

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>[D3DX11_FFT_MAX_DIMENSIONS]</b>


            Length of each dimension in the FFT.
          


### -field DimensionMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Combination of <a href="https://msdn.microsoft.com/5623b0e6-73f0-4d89-bf3e-a116409b369e">D3DX11_FFT_DIM_MASK</a> flags indicating the  dimensions to transform.
          


### -field Type

Type: <b><a href="https://msdn.microsoft.com/a9e2cf90-cef0-44af-9863-f8f742673950">D3DX11_FFT_DATA_TYPE</a></b>


<a href="https://msdn.microsoft.com/a9e2cf90-cef0-44af-9863-f8f742673950">D3DX11_FFT_DATA_TYPE</a> flag indicating the type of data being transformed.
          


## -see-also




<a href="https://msdn.microsoft.com/ED42B8D1-F4C9-489F-999B-A53BC96BA337">D3DCSX 11 Structures</a>
 

 

