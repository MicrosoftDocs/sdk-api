---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.AddLoggingUrl
title: IWMReaderNetworkConfig::AddLoggingUrl (wmsdkidl.h)
description: The AddLoggingUrl method specifies a server that receive logging information from the reader object.
helpviewer_keywords: ["AddLoggingUrl","AddLoggingUrl method [windows Media Format]","AddLoggingUrl method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","AddLoggingUrl method","IWMReaderNetworkConfig.AddLoggingUrl","IWMReaderNetworkConfig::AddLoggingUrl","IWMReaderNetworkConfigAddLoggingUrl","wmformat.iwmreadernetworkconfig_addloggingurl","wmsdkidl/IWMReaderNetworkConfig::AddLoggingUrl"]
old-location: wmformat\iwmreadernetworkconfig_addloggingurl.htm
tech.root: wmformat
ms.assetid: 471b17c8-20e4-44f3-88ee-48a35cd8930c
ms.date: 4/26/2023
ms.keywords: AddLoggingUrl, AddLoggingUrl method [windows Media Format], AddLoggingUrl method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],AddLoggingUrl method, IWMReaderNetworkConfig.AddLoggingUrl, IWMReaderNetworkConfig::AddLoggingUrl, IWMReaderNetworkConfigAddLoggingUrl, wmformat.iwmreadernetworkconfig_addloggingurl, wmsdkidl/IWMReaderNetworkConfig::AddLoggingUrl
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
 - IWMReaderNetworkConfig::AddLoggingUrl
 - wmsdkidl/IWMReaderNetworkConfig::AddLoggingUrl
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
 - IWMReaderNetworkConfig.AddLoggingUrl
---

# IWMReaderNetworkConfig::AddLoggingUrl


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddLoggingUrl</b> method specifies a server that receive logging information from the reader object.

## -parameters

### -param pwszUrl [in]

Specifies a string containing the URL.

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
Null value passed in to <i>pwszUrl</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to create or add the URL.

</td>
</tr>
</table>

## -remarks

When the reader streams content from a server, it automatically sends logging information to that server. Use the <b>AddLoggingUrl</b> method to specify additional servers that will receive the logging information.

## -see-also

<a href="/windows/desktop/wmformat/client">Client Logging</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>