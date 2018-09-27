---
UID: NF:strmif.IAMVideoControl.GetMaxAvailableFrameRate
title: IAMVideoControl::GetMaxAvailableFrameRate
author: windows-sdk-content
description: The GetMaxAvailableFrameRate method retrieves the maximum frame rate currently available, based on bus bandwidth usage for connections, such as USB and IEEE 1394, where the maximum frame rate may be limited by bandwidth availability.
old-location: dshow\iamvideocontrol_getmaxavailableframerate.htm
tech.root: DirectShow
ms.assetid: a196cf6e-491c-4d01-abfe-831440e75058
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetMaxAvailableFrameRate, GetMaxAvailableFrameRate method [DirectShow], GetMaxAvailableFrameRate method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetMaxAvailableFrameRate method, IAMVideoControl.GetMaxAvailableFrameRate, IAMVideoControl::GetMaxAvailableFrameRate, IAMVideoControlGetMaxAvailableFrameRate, dshow.iamvideocontrol_getmaxavailableframerate, strmif/IAMVideoControl::GetMaxAvailableFrameRate
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAMVideoControl.GetMaxAvailableFrameRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoControl::GetMaxAvailableFrameRate


## -description



The <code>GetMaxAvailableFrameRate</code> method retrieves the maximum frame rate currently available, based on bus bandwidth usage for connections, such as USB and IEEE 1394, where the maximum frame rate may be limited by bandwidth availability.




## -parameters




### -param pPin [in]

Pointer to the pin to retrieve the maximum frame rate from.


### -param iIndex [in]

Index of the format to query for maximum frame rate. This index corresponds to the order in which formats are enumerated by <a href="https://msdn.microsoft.com/9dd84847-2cae-42f2-a858-7106cd2ac075">IAMStreamConfig::GetStreamCaps</a>. The value must range between zero and the number of supported <b>VIDEO_STREAM_CONFIG_CAPS</b> structures returned by <a href="https://msdn.microsoft.com/355b8c4c-6d07-4d31-8dc5-ddc5ec2bf1cd">IAMStreamConfig::GetNumberOfCapabilities</a>) minus one.


### -param Dimensions [in]

Frame image size (width and height) in pixels.


### -param MaxAvailableFrameRate [out]

Pointer to the maximum available frame rate. The frame rate is expressed as frame duration in 100-nanosecond units.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bd114977-c76c-4429-a835-98601b350a93">IAMVideoControl Interface</a>



<a href="https://msdn.microsoft.com/c4e68065-79d0-4e2e-abe5-2e5b6a51bd40">VIDEO_STREAM_CONFIG_CAPS Structure</a>
 

 

