---
UID: NF:wmsdkidl.IWMWriterNetworkSink.GetMaximumClients
title: IWMWriterNetworkSink::GetMaximumClients (wmsdkidl.h)
description: The GetMaximumClients method retrieves the maximum number of clients that can connect to this sink.
helpviewer_keywords: ["GetMaximumClients","GetMaximumClients method [windows Media Format]","GetMaximumClients method [windows Media Format]","IWMWriterNetworkSink interface","IWMWriterNetworkSink interface [windows Media Format]","GetMaximumClients method","IWMWriterNetworkSink.GetMaximumClients","IWMWriterNetworkSink::GetMaximumClients","IWMWriterNetworkSinkGetMaximumClients","wmformat.iwmwriternetworksink_getmaximumclients","wmsdkidl/IWMWriterNetworkSink::GetMaximumClients"]
old-location: wmformat\iwmwriternetworksink_getmaximumclients.htm
tech.root: wmformat
ms.assetid: c0ef3fd6-aed7-40ec-96e6-7962e77bdd46
ms.date: 4/26/2023
ms.keywords: GetMaximumClients, GetMaximumClients method [windows Media Format], GetMaximumClients method [windows Media Format],IWMWriterNetworkSink interface, IWMWriterNetworkSink interface [windows Media Format],GetMaximumClients method, IWMWriterNetworkSink.GetMaximumClients, IWMWriterNetworkSink::GetMaximumClients, IWMWriterNetworkSinkGetMaximumClients, wmformat.iwmwriternetworksink_getmaximumclients, wmsdkidl/IWMWriterNetworkSink::GetMaximumClients
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
 - IWMWriterNetworkSink::GetMaximumClients
 - wmsdkidl/IWMWriterNetworkSink::GetMaximumClients
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
 - IWMWriterNetworkSink.GetMaximumClients
---

# IWMWriterNetworkSink::GetMaximumClients


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMaximumClients</b> method retrieves the maximum number of clients that can connect to this sink.

## -parameters

### -param pdwMaxClients [out]

Pointer to a variable that receives the maximum number of clients. The default value is 5.

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
<i>pdwMaxClients</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink">IWMWriterNetworkSink Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients">IWMWriterNetworkSink::SetMaximumClients</a>