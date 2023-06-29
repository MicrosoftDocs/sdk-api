---
UID: NF:wmsdkidl.IWMBandwidthSharing.SetBandwidth
title: IWMBandwidthSharing::SetBandwidth (wmsdkidl.h)
description: The SetBandwidth method sets the bandwidth and maximum buffer size for a combined stream.
helpviewer_keywords: ["IWMBandwidthSharing interface [windows Media Format]","SetBandwidth method","IWMBandwidthSharing.SetBandwidth","IWMBandwidthSharing::SetBandwidth","IWMBandwidthSharingSetBandwidth","SetBandwidth","SetBandwidth method [windows Media Format]","SetBandwidth method [windows Media Format]","IWMBandwidthSharing interface","wmformat.iwmbandwidthsharing_setbandwidth","wmsdkidl/IWMBandwidthSharing::SetBandwidth"]
old-location: wmformat\iwmbandwidthsharing_setbandwidth.htm
tech.root: wmformat
ms.assetid: 1f2ac613-3674-46d9-ae7c-26389dbede02
ms.date: 4/26/2023
ms.keywords: IWMBandwidthSharing interface [windows Media Format],SetBandwidth method, IWMBandwidthSharing.SetBandwidth, IWMBandwidthSharing::SetBandwidth, IWMBandwidthSharingSetBandwidth, SetBandwidth, SetBandwidth method [windows Media Format], SetBandwidth method [windows Media Format],IWMBandwidthSharing interface, wmformat.iwmbandwidthsharing_setbandwidth, wmsdkidl/IWMBandwidthSharing::SetBandwidth
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMBandwidthSharing::SetBandwidth
 - wmsdkidl/IWMBandwidthSharing::SetBandwidth
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
 - IWMBandwidthSharing.SetBandwidth
---

# IWMBandwidthSharing::SetBandwidth


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetBandwidth</b> method sets the bandwidth and maximum buffer size for a combined stream.

## -parameters

### -param dwBitrate [in]

<b>DWORD</b> containing the bit rate in bits per second. The combined bandwidths of the streams cannot exceed this value.

### -param msBufferWindow [in]

Specifies the buffer window in milliseconds. The combined buffer sizes of the streams cannot exceed this value.

## -returns

This method always returns S_OK.

## -remarks

The settings of a bandwidth sharing object are purely informational. They are not checked for accuracy.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-getbandwidth">IWMBandwidthSharing::GetBandwidth</a>