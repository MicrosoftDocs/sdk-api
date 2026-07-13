---
UID: NF:wmsdkidl.IWMWriterNetworkSink.Open
title: IWMWriterNetworkSink::Open (wmsdkidl.h)
description: The Open method opens a network port, and starts listening for network connections.
helpviewer_keywords: ["IWMWriterNetworkSink interface [windows Media Format]","Open method","IWMWriterNetworkSink.Open","IWMWriterNetworkSink::Open","IWMWriterNetworkSinkOpen","Open","Open method [windows Media Format]","Open method [windows Media Format]","IWMWriterNetworkSink interface","wmformat.iwmwriternetworksink_open","wmsdkidl/IWMWriterNetworkSink::Open"]
old-location: wmformat\iwmwriternetworksink_open.htm
tech.root: wmformat
ms.assetid: 2cfd4693-794c-46c8-b72d-b7529c63f16e
ms.date: 4/26/2023
ms.keywords: IWMWriterNetworkSink interface [windows Media Format],Open method, IWMWriterNetworkSink.Open, IWMWriterNetworkSink::Open, IWMWriterNetworkSinkOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMWriterNetworkSink interface, wmformat.iwmwriternetworksink_open, wmsdkidl/IWMWriterNetworkSink::Open
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
 - IWMWriterNetworkSink::Open
 - wmsdkidl/IWMWriterNetworkSink::Open
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
 - IWMWriterNetworkSink.Open
---

# IWMWriterNetworkSink::Open


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Open</b> method opens a network port, and starts listening for network connections.

## -parameters

### -param pdwPortNum [in, out]

On input, pointer to a variable that specifies the port number. Set this value to zero if you want the network sink to select a suitable port. On output, the variable receives the port number that was used.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, the values shown in the following table.

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
The <i>pdwPortNum</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The network sink is already open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NETWORK_RESOURCE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The port number specified is already in use.

</td>
</tr>
</table>

## -remarks

This method binds the port. To release the port, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close">IWMWriterNetworkSink::Close</a>.

See the Remarks and Example Code sections for <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink">IWMWriterNetworkSink Interface</a>