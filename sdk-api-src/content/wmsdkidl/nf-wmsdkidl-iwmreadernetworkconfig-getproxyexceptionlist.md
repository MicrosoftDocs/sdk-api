---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetProxyExceptionList
title: IWMReaderNetworkConfig::GetProxyExceptionList (wmsdkidl.h)
description: The GetProxyExceptionList method retrieves the list of computers, domains, or addresses for which the reader object bypasses the proxy server.
helpviewer_keywords: ["GetProxyExceptionList","GetProxyExceptionList method [windows Media Format]","GetProxyExceptionList method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetProxyExceptionList method","IWMReaderNetworkConfig.GetProxyExceptionList","IWMReaderNetworkConfig::GetProxyExceptionList","IWMReaderNetworkConfigGetProxyExceptionList","wmformat.iwmreadernetworkconfig_getproxyexceptionlist","wmsdkidl/IWMReaderNetworkConfig::GetProxyExceptionList"]
old-location: wmformat\iwmreadernetworkconfig_getproxyexceptionlist.htm
tech.root: wmformat
ms.assetid: 90cf6e58-8666-4bab-974e-a7e999aeddf1
ms.date: 4/26/2023
ms.keywords: GetProxyExceptionList, GetProxyExceptionList method [windows Media Format], GetProxyExceptionList method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetProxyExceptionList method, IWMReaderNetworkConfig.GetProxyExceptionList, IWMReaderNetworkConfig::GetProxyExceptionList, IWMReaderNetworkConfigGetProxyExceptionList, wmformat.iwmreadernetworkconfig_getproxyexceptionlist, wmsdkidl/IWMReaderNetworkConfig::GetProxyExceptionList
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
 - IWMReaderNetworkConfig::GetProxyExceptionList
 - wmsdkidl/IWMReaderNetworkConfig::GetProxyExceptionList
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
 - IWMReaderNetworkConfig.GetProxyExceptionList
---

# IWMReaderNetworkConfig::GetProxyExceptionList


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetProxyExceptionList</b> method retrieves the list of computers, domains, or addresses for which the reader object bypasses the proxy server.

## -parameters

### -param pwszProtocol [in]

Pointer to a string that contains a protocol name, such as "http" or "mms". The string is not case-sensitive.

### -param pwszExceptionList [out]

Pointer to a buffer that receives a string containing the exception list. The returned string is a comma-separated list. For more information, see <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyexceptionlist">SetProxyExceptionList</a>. The list applies only to the protocol specified in <i>pwszProtocol</i>; the reader object supports separate settings for each protocol.

### -param pcchExceptionList [in, out]

On input, pointer to a variable specifying the size of the <i>pwszExceptionList</i> buffer, in characters. On output, the variable contains the length of the string, including the terminating <b>null</b> character.

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
The size of the buffer passed in is not large enough to hold the return string.

</td>
</tr>
</table>

## -remarks

Call this method twice. The first time, pass <b>NULL</b> as the value for <i>pwszExceptionList</i>. The method returns the size of the string in the <i>pcchExceptionList</i> parameter. Allocate the required amount of memory for the string and call the method again. This time, pass a pointer to the allocated buffer in the <i>pwszExceptionList</i> parameter.

For more information, see the Remarks for <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyexceptionlist">SetProxyExceptionList</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxyexceptionlist">IWMReaderNetworkConfig::SetProxyExceptionList</a>