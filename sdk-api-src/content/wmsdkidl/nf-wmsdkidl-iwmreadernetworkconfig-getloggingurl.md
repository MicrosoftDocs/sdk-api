---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetLoggingUrl
title: IWMReaderNetworkConfig::GetLoggingUrl (wmsdkidl.h)
description: The GetLoggingUrl method retrieves a URL from the list of servers that receive logging information from the reader object. Use the IWMReaderNetworkConfig::GetLoggingUrl method to add servers to the list.
helpviewer_keywords: ["GetLoggingUrl","GetLoggingUrl method [windows Media Format]","GetLoggingUrl method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetLoggingUrl method","IWMReaderNetworkConfig.GetLoggingUrl","IWMReaderNetworkConfig::GetLoggingUrl","IWMReaderNetworkConfigGetLoggingUrl","wmformat.iwmreadernetworkconfig_getloggingurl","wmsdkidl/IWMReaderNetworkConfig::GetLoggingUrl"]
old-location: wmformat\iwmreadernetworkconfig_getloggingurl.htm
tech.root: wmformat
ms.assetid: 27c5a97b-e04b-4d15-b19a-3c0d78feee95
ms.date: 4/26/2023
ms.keywords: GetLoggingUrl, GetLoggingUrl method [windows Media Format], GetLoggingUrl method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetLoggingUrl method, IWMReaderNetworkConfig.GetLoggingUrl, IWMReaderNetworkConfig::GetLoggingUrl, IWMReaderNetworkConfigGetLoggingUrl, wmformat.iwmreadernetworkconfig_getloggingurl, wmsdkidl/IWMReaderNetworkConfig::GetLoggingUrl
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
 - IWMReaderNetworkConfig::GetLoggingUrl
 - wmsdkidl/IWMReaderNetworkConfig::GetLoggingUrl
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
 - IWMReaderNetworkConfig.GetLoggingUrl
---

# IWMReaderNetworkConfig::GetLoggingUrl


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetLoggingUrl</b> method retrieves a URL from the list of servers that receive logging information from the reader object. Use the <b>IWMReaderNetworkConfig::GetLoggingUrl</b> method to add servers to the list.

## -parameters

### -param dwIndex [in]

Specifies which URL to retrieve, indexed from zero. To get the number of URLs, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getloggingurlcount">IWMReaderNetworkConfig::GetLoggingUrlCount</a> method.

### -param pwszUrl [out]

Pointer to a buffer that receives a string containing the URL. The caller must allocate the buffer.

### -param pcchUrl [in, out]

On input, specifies the length of the <i>pwszUrl</i> buffer, in characters. On output, receives the length of the URL, including the terminating <b>null</b> character.

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
<b>NULL</b> or invalid argument passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
Size passed in to <i>pcchUrl</i> is too small.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetLoggingUrl</b>. On the first call, pass <b>NULL</b> for <i>pwszUrl</i>. On return, the value pointed to by <i>pcchUrl</i> is set to the number of wide characters, including the terminating <b>null</b>, required to hold the URL. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszUrl</i> on the second call.

## -see-also

<a href="/windows/desktop/wmformat/client">Client Logging</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>