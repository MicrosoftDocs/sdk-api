---
UID: NF:strmif.IAMVideoControl.GetFrameRateList
title: IAMVideoControl::GetFrameRateList (strmif.h)
author: windows-sdk-content
description: The GetFrameRateList method retrieves a list of available frame rates.
old-location: dshow\iamvideocontrol_getframeratelist.htm
tech.root: DirectShow
ms.assetid: 864f294f-1a18-4d4c-952e-1965da4c9496
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFrameRateList, GetFrameRateList method [DirectShow], GetFrameRateList method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetFrameRateList method, IAMVideoControl.GetFrameRateList, IAMVideoControl::GetFrameRateList, IAMVideoControlGetFrameRateList, dshow.iamvideocontrol_getframeratelist, strmif/IAMVideoControl::GetFrameRateList
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoControl.GetFrameRateList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

