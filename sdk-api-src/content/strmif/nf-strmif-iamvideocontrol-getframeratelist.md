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

# IAMVideoControl::GetFrameRateList


## -description



The <code>GetFrameRateList</code> method retrieves a list of available frame rates.




## -parameters




### -param pPin [in]

Pointer to the pin to query for the list of frame rates.


### -param iIndex [in]

Index of the format to query for frame rates. This index corresponds to the order in which formats are enumerated by <a href="https://msdn.microsoft.com/9dd84847-2cae-42f2-a858-7106cd2ac075">IAMStreamConfig::GetStreamCaps</a>. The value must range between zero and the number of supported <a href="https://msdn.microsoft.com/c4e68065-79d0-4e2e-abe5-2e5b6a51bd40">VIDEO_STREAM_CONFIG_CAPS</a> structures returned by <a href="https://msdn.microsoft.com/355b8c4c-6d07-4d31-8dc5-ddc5ec2bf1cd">IAMStreamConfig::GetNumberOfCapabilities</a>) minus one.


### -param Dimensions [in]

Frame image size (width and height) in pixels.


### -param ListSize [out]

Pointer to the number of elements in the list of frame rates.


### -param FrameRates [out]

Address of a pointer to an array of frame rates in 100-nanosecond units. Can be <b>NULL</b> if you only need <i>ListSize</i>.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



The caller is responsible for freeing the memory through a call to <b>CoTaskMemFree</b>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bd114977-c76c-4429-a835-98601b350a93">IAMVideoControl Interface</a>



<a href="https://msdn.microsoft.com/c4e68065-79d0-4e2e-abe5-2e5b6a51bd40">VIDEO_STREAM_CONFIG_CAPS Structure</a>
 

 

