---
UID: NF:wmsdkidl.IWMStreamConfig.SetBitrate
title: IWMStreamConfig::SetBitrate (wmsdkidl.h)
description: The SetBitrate method specifies the bit rate for the stream.
helpviewer_keywords: ["IWMStreamConfig interface [windows Media Format]","SetBitrate method","IWMStreamConfig.SetBitrate","IWMStreamConfig::SetBitrate","IWMStreamConfigSetBitrate","SetBitrate","SetBitrate method [windows Media Format]","SetBitrate method [windows Media Format]","IWMStreamConfig interface","wmformat.iwmstreamconfig_setbitrate","wmsdkidl/IWMStreamConfig::SetBitrate"]
old-location: wmformat\iwmstreamconfig_setbitrate.htm
tech.root: wmformat
ms.assetid: 202be688-e739-4e80-9574-f85b2eb168fc
ms.date: 12/05/2018
ms.keywords: IWMStreamConfig interface [windows Media Format],SetBitrate method, IWMStreamConfig.SetBitrate, IWMStreamConfig::SetBitrate, IWMStreamConfigSetBitrate, SetBitrate, SetBitrate method [windows Media Format], SetBitrate method [windows Media Format],IWMStreamConfig interface, wmformat.iwmstreamconfig_setbitrate, wmsdkidl/IWMStreamConfig::SetBitrate
f1_keywords:
- wmsdkidl/IWMStreamConfig.SetBitrate
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStreamConfig::SetBitrate


## -description



The <b>SetBitrate</b> method specifies the bit rate for the stream.




## -parameters




### -param pdwBitrate [in]

<b>DWORD</b> containing the bit rate, in bits per second.


## -returns



This method always returns S_OK.




## -remarks



The bit rate is the number of bits per second given to the stream in the ASF file, not including any overhead. For compressed bit streams, such as audio or video, a higher bit rate gives higher quality.

The new value will not take effect in the profile until you call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getbitrate">IWMStreamConfig::GetBitrate</a>
 

 

