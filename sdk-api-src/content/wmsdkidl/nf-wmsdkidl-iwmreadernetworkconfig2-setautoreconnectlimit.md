---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.SetAutoReconnectLimit
title: IWMReaderNetworkConfig2::SetAutoReconnectLimit (wmsdkidl.h)
description: The SetAutoReconnectLimit method sets the maximum number of times the reader will attempt to reconnect to the server in the case of an unexpected disconnection.
helpviewer_keywords: ["IWMReaderNetworkConfig2 interface [windows Media Format]","SetAutoReconnectLimit method","IWMReaderNetworkConfig2.SetAutoReconnectLimit","IWMReaderNetworkConfig2::SetAutoReconnectLimit","IWMReaderNetworkConfig2SetAutoReconnectLimit","SetAutoReconnectLimit","SetAutoReconnectLimit method [windows Media Format]","SetAutoReconnectLimit method [windows Media Format]","IWMReaderNetworkConfig2 interface","wmformat.iwmreadernetworkconfig2_setautoreconnectlimit","wmsdkidl/IWMReaderNetworkConfig2::SetAutoReconnectLimit"]
old-location: wmformat\iwmreadernetworkconfig2_setautoreconnectlimit.htm
tech.root: wmformat
ms.assetid: 0ef6bb5c-6369-4b80-a227-da790b1ab6da
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig2 interface [windows Media Format],SetAutoReconnectLimit method, IWMReaderNetworkConfig2.SetAutoReconnectLimit, IWMReaderNetworkConfig2::SetAutoReconnectLimit, IWMReaderNetworkConfig2SetAutoReconnectLimit, SetAutoReconnectLimit, SetAutoReconnectLimit method [windows Media Format], SetAutoReconnectLimit method [windows Media Format],IWMReaderNetworkConfig2 interface, wmformat.iwmreadernetworkconfig2_setautoreconnectlimit, wmsdkidl/IWMReaderNetworkConfig2::SetAutoReconnectLimit
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
 - IWMReaderNetworkConfig2::SetAutoReconnectLimit
 - wmsdkidl/IWMReaderNetworkConfig2::SetAutoReconnectLimit
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
 - IWMReaderNetworkConfig2.SetAutoReconnectLimit
---

# IWMReaderNetworkConfig2::SetAutoReconnectLimit


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAutoReconnectLimit</b> method sets the maximum number of times the reader will attempt to reconnect to the server in the case of an unexpected disconnection. This feature, called Fast Reconnect, applies only to content being streamed from a server running Windows Media Services.

## -parameters

### -param dwAutoReconnectLimit [in]

Specifies the maximum number of times the reader object will attempt to reconnect. To disable automatic reconnection, set this value to zero.

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

The method configures the Fast Reconnect feature, which enables the reader object to reconnect to the server automatically if it loses the connection. When possible, playback resumes at the same point in the stream. The accuracy may depend on whether the source file is indexed. For live content, there may be a gap in the stream.

The reader only tries to reconnect if the interruption is unexpected. For example, it does not try to reconnect if the server denies access because of an authentication failure, if the server terminates the connection because of client inactivity, if the server administrator terminates the connection, and so forth.

This method is equivalent to setting the WMReconnect modifier in the URL. For example:

mms://MyServer/MyVideo.wmv?WMReconnect=5

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2">IWMReaderNetworkConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getautoreconnectlimit">IWMReaderNetworkConfig2::GetAutoReconnectLimit</a>