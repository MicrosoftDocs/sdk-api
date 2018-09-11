---
UID: NF:wmsdkidl.IWMStreamConfig.SetBitrate
title: IWMStreamConfig::SetBitrate
author: windows-sdk-content
description: The SetBitrate method specifies the bit rate for the stream.
old-location: wmformat\iwmstreamconfig_setbitrate.htm
tech.root: wmformat
ms.assetid: 202be688-e739-4e80-9574-f85b2eb168fc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMStreamConfig interface [windows Media Format],SetBitrate method, IWMStreamConfig.SetBitrate, IWMStreamConfig::SetBitrate, IWMStreamConfigSetBitrate, SetBitrate, SetBitrate method [windows Media Format], SetBitrate method [windows Media Format],IWMStreamConfig interface, wmformat.iwmstreamconfig_setbitrate, wmsdkidl/IWMStreamConfig::SetBitrate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMStreamConfig.SetBitrate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMStreamConfig::SetBitrate


## -description



The <b>SetBitrate</b> method specifies the bit rate for the stream.




## -parameters




### -param pdwBitrate

TBD




#### - dwBitrate [in]

<b>DWORD</b> containing the bit rate, in bits per second.


## -returns



This method always returns S_OK.




## -remarks



The bit rate is the number of bits per second given to the stream in the ASF file, not including any overhead. For compressed bit streams, such as audio or video, a higher bit rate gives higher quality.

The new value will not take effect in the profile until you call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>



<a href="https://msdn.microsoft.com/d34bea45-758e-4c4a-928f-229ce6b4241c">IWMStreamConfig::GetBitrate</a>
 

 

