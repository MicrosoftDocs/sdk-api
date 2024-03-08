---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetEnableThinning
title: IWMReaderNetworkConfig2::GetEnableThinning (wmsdkidl.h)
description: The GetEnableThinning method ascertains whether Intelligent Streaming is enabled. Intelligent Streaming is the communication between the reader and the streaming server that enables the server to change the content sent based on available bandwidth.
helpviewer_keywords: ["GetEnableThinning","GetEnableThinning method [windows Media Format]","GetEnableThinning method [windows Media Format]","IWMReaderNetworkConfig2 interface","IWMReaderNetworkConfig2 interface [windows Media Format]","GetEnableThinning method","IWMReaderNetworkConfig2.GetEnableThinning","IWMReaderNetworkConfig2::GetEnableThinning","IWMReaderNetworkConfig2GetEnableThinning","wmformat.iwmreadernetworkconfig2_getenablethinning","wmsdkidl/IWMReaderNetworkConfig2::GetEnableThinning"]
old-location: wmformat\iwmreadernetworkconfig2_getenablethinning.htm
tech.root: wmformat
ms.assetid: 3ad43406-56db-48db-96a7-419b6719dbd4
ms.date: 4/26/2023
ms.keywords: GetEnableThinning, GetEnableThinning method [windows Media Format], GetEnableThinning method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetEnableThinning method, IWMReaderNetworkConfig2.GetEnableThinning, IWMReaderNetworkConfig2::GetEnableThinning, IWMReaderNetworkConfig2GetEnableThinning, wmformat.iwmreadernetworkconfig2_getenablethinning, wmsdkidl/IWMReaderNetworkConfig2::GetEnableThinning
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
 - IWMReaderNetworkConfig2::GetEnableThinning
 - wmsdkidl/IWMReaderNetworkConfig2::GetEnableThinning
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
 - IWMReaderNetworkConfig2.GetEnableThinning
---

# IWMReaderNetworkConfig2::GetEnableThinning


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetEnableThinning</b> method ascertains whether Intelligent Streaming is enabled. Intelligent Streaming is the communication between the reader and the streaming server that enables the server to change the content sent based on available bandwidth.

## -parameters

### -param pfEnableThinning [out]

Pointer to a variable that receives a Boolean value. The value is <b>TRUE</b> if thinning is enabled, or <b>FALSE</b> if thinning is disabled.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>

## -remarks

With Intelligent Streaming enabled, the reader responds to insufficient bandwidth by requesting that the server reduce the bit rate by using one of the following techniques. If one technique does not solve the problem, the reader will try the next one:

<ul>
<li>If the file is encoded using multiple bit rates (MBR), the first step the reader takes to rectify insufficient bandwidth is to request a lower bit rate version of streams.</li>
<li>If the file is not MBR, or if using a lower bit rate stream does not reduce the bandwidth requirements enough, the reader requests that the server thin the video streams. This means that the server reduces the frame rate of the video being streamed.</li>
<li>If thinning the video streams does not reduce the bandwidth requirements enough, the reader requests that the server stop sending video streams.</li>
</ul>
If Intelligent Streaming is disabled by setting <i>pfEnableThinning</i> to <b>FALSE</b>, the reader will not request any bandwidth corrections.

This feature applies only to content streaming from a server running Windows Media Services.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2">IWMReaderNetworkConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablethinning">IWMReaderNetworkConfig2::SetEnableThinning</a>