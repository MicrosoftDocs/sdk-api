---
UID: NF:wmsdkidl.IWMWriterNetworkSink.GetHostURL
title: IWMWriterNetworkSink::GetHostURL (wmsdkidl.h)
description: The GetHostURL method retrieves the URL from which the stream is broadcast. Clients will access the stream from this URL.
helpviewer_keywords: ["GetHostURL","GetHostURL method [windows Media Format]","GetHostURL method [windows Media Format]","IWMWriterNetworkSink interface","IWMWriterNetworkSink interface [windows Media Format]","GetHostURL method","IWMWriterNetworkSink.GetHostURL","IWMWriterNetworkSink::GetHostURL","IWMWriterNetworkSinkGetHostURL","wmformat.iwmwriternetworksink_gethosturl","wmsdkidl/IWMWriterNetworkSink::GetHostURL"]
old-location: wmformat\iwmwriternetworksink_gethosturl.htm
tech.root: wmformat
ms.assetid: 66d4747e-aec5-47bd-ac4a-dc052e964601
ms.date: 4/26/2023
ms.keywords: GetHostURL, GetHostURL method [windows Media Format], GetHostURL method [windows Media Format],IWMWriterNetworkSink interface, IWMWriterNetworkSink interface [windows Media Format],GetHostURL method, IWMWriterNetworkSink.GetHostURL, IWMWriterNetworkSink::GetHostURL, IWMWriterNetworkSinkGetHostURL, wmformat.iwmwriternetworksink_gethosturl, wmsdkidl/IWMWriterNetworkSink::GetHostURL
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
 - IWMWriterNetworkSink::GetHostURL
 - wmsdkidl/IWMWriterNetworkSink::GetHostURL
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
 - IWMWriterNetworkSink.GetHostURL
---

# IWMWriterNetworkSink::GetHostURL


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetHostURL</b> method retrieves the URL from which the stream is broadcast. Clients will access the stream from this URL.

## -parameters

### -param pwszURL [out]

Pointer to buffer that receives a string containing the URL. To retrieve the length of the string, set this parameter to <b>NULL</b>.

### -param pcchURL [in, out]

On input, pointer to the size of <i>pwszURL</i>, in characters. On output, this parameter receives the length of the URL in characters, including the terminating <b>null</b> character.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, the values shown in the following table.

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
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>pcchURL</i> cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The network sink is not connected.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetHostURL</b>. On the first call, pass <b>NULL</b> as <i>pwszURL</i>. On return, the value pointed to by <i>pcchURL</i> is set to the number of characters, including the terminating <b>null</b> character, required to hold the URL. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszURL</i> on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink">IWMWriterNetworkSink Interface</a>