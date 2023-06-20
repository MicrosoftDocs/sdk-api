---
UID: NF:wmsdkidl.IWMStreamConfig.SetBitrate
title: IWMStreamConfig::SetBitrate (wmsdkidl.h)
description: The SetBitrate method specifies the bit rate for the stream.
helpviewer_keywords: ["IWMStreamConfig interface [windows Media Format]","SetBitrate method","IWMStreamConfig.SetBitrate","IWMStreamConfig::SetBitrate","IWMStreamConfigSetBitrate","SetBitrate","SetBitrate method [windows Media Format]","SetBitrate method [windows Media Format]","IWMStreamConfig interface","wmformat.iwmstreamconfig_setbitrate","wmsdkidl/IWMStreamConfig::SetBitrate"]
old-location: wmformat\iwmstreamconfig_setbitrate.htm
tech.root: wmformat
ms.assetid: 202be688-e739-4e80-9574-f85b2eb168fc
ms.date: 4/26/2023
ms.keywords: IWMStreamConfig interface [windows Media Format],SetBitrate method, IWMStreamConfig.SetBitrate, IWMStreamConfig::SetBitrate, IWMStreamConfigSetBitrate, SetBitrate, SetBitrate method [windows Media Format], SetBitrate method [windows Media Format],IWMStreamConfig interface, wmformat.iwmstreamconfig_setbitrate, wmsdkidl/IWMStreamConfig::SetBitrate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMStreamConfig::SetBitrate
 - wmsdkidl/IWMStreamConfig::SetBitrate
dev_langs:
 - c++
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
---

# IWMStreamConfig::SetBitrate


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetBitrate</b> method specifies the bit rate for the stream.

## -parameters

### -param pdwBitrate [in]

<b>DWORD</b> containing the bit rate, in bits per second.

## -returns

This method always returns S_OK.

## -remarks

The bit rate is the number of bits per second given to the stream in the ASF file, not including any overhead. For compressed bit streams, such as audio or video, a higher bit rate gives higher quality.

The new value will not take effect in the profile until you call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getbitrate">IWMStreamConfig::GetBitrate</a>