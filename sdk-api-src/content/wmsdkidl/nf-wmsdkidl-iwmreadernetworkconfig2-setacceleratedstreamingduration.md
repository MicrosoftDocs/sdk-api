---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.SetAcceleratedStreamingDuration
title: IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration (wmsdkidl.h)
description: The SetAcceleratedStreamingDuration method sets the accelerated streaming duration. This duration applies to the Fast Start feature of Windows Media Services, which enables content to be played quickly without waiting for lengthy initial buffering.
helpviewer_keywords: ["IWMReaderNetworkConfig2 interface [windows Media Format]","SetAcceleratedStreamingDuration method","IWMReaderNetworkConfig2.SetAcceleratedStreamingDuration","IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration","IWMReaderNetworkConfig2SetAcceleratedStreamingDuration","SetAcceleratedStreamingDuration","SetAcceleratedStreamingDuration method [windows Media Format]","SetAcceleratedStreamingDuration method [windows Media Format]","IWMReaderNetworkConfig2 interface","wmformat.iwmreadernetworkconfig2_setacceleratedstreamingduration","wmsdkidl/IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration"]
old-location: wmformat\iwmreadernetworkconfig2_setacceleratedstreamingduration.htm
tech.root: wmformat
ms.assetid: c9ad5064-7742-4145-b560-f3e867da609a
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig2 interface [windows Media Format],SetAcceleratedStreamingDuration method, IWMReaderNetworkConfig2.SetAcceleratedStreamingDuration, IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration, IWMReaderNetworkConfig2SetAcceleratedStreamingDuration, SetAcceleratedStreamingDuration, SetAcceleratedStreamingDuration method [windows Media Format], SetAcceleratedStreamingDuration method [windows Media Format],IWMReaderNetworkConfig2 interface, wmformat.iwmreadernetworkconfig2_setacceleratedstreamingduration, wmsdkidl/IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration
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
 - IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration
 - wmsdkidl/IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration
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
 - IWMReaderNetworkConfig2.SetAcceleratedStreamingDuration
---

# IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAcceleratedStreamingDuration</b> method sets the accelerated streaming duration. This duration applies to the Fast Start feature of Windows Media Services, which enables content to be played quickly without waiting for lengthy initial buffering.

## -parameters

### -param cnsAccelDuration [in]

Specifies the accelerated streaming duration, in 100-nanosecond units. The maximum value is 1,200,000,000. This is the amount of data at the beginning of the content that is streamed at an accelerated rate.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

When using Fast Start, the server running Windows Media Services will send some data at the beginning of the content at a faster rate than that specified by the bit rate of the content.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2">IWMReaderNetworkConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getacceleratedstreamingduration">IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration</a>