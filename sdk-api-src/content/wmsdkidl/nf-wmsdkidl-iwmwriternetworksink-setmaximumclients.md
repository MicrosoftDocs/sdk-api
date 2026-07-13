---
UID: NF:wmsdkidl.IWMWriterNetworkSink.SetMaximumClients
title: IWMWriterNetworkSink::SetMaximumClients (wmsdkidl.h)
description: The SetMaximumClients method sets the maximum number of clients that can connect to this sink. Call this method before streaming begins.
helpviewer_keywords: ["IWMWriterNetworkSink interface [windows Media Format]","SetMaximumClients method","IWMWriterNetworkSink.SetMaximumClients","IWMWriterNetworkSink::SetMaximumClients","IWMWriterNetworkSinkSetMaximumClients","SetMaximumClients","SetMaximumClients method [windows Media Format]","SetMaximumClients method [windows Media Format]","IWMWriterNetworkSink interface","wmformat.iwmwriternetworksink_setmaximumclients","wmsdkidl/IWMWriterNetworkSink::SetMaximumClients"]
old-location: wmformat\iwmwriternetworksink_setmaximumclients.htm
tech.root: wmformat
ms.assetid: 619f0684-28bb-4412-acbf-27434672083a
ms.date: 4/26/2023
ms.keywords: IWMWriterNetworkSink interface [windows Media Format],SetMaximumClients method, IWMWriterNetworkSink.SetMaximumClients, IWMWriterNetworkSink::SetMaximumClients, IWMWriterNetworkSinkSetMaximumClients, SetMaximumClients, SetMaximumClients method [windows Media Format], SetMaximumClients method [windows Media Format],IWMWriterNetworkSink interface, wmformat.iwmwriternetworksink_setmaximumclients, wmsdkidl/IWMWriterNetworkSink::SetMaximumClients
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
 - IWMWriterNetworkSink::SetMaximumClients
 - wmsdkidl/IWMWriterNetworkSink::SetMaximumClients
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
 - IWMWriterNetworkSink.SetMaximumClients
---

# IWMWriterNetworkSink::SetMaximumClients


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetMaximumClients</b> method sets the maximum number of clients that can connect to this sink. Call this method before streaming begins.

## -parameters

### -param dwMaxClients [in]

Specifies the maximum number of clients. The value must be from 0 to 50, inclusive. The default value is 5.

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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Streaming has already begun, or the value of <i>dwMaxClients</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink">IWMWriterNetworkSink Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-getmaximumclients">IWMWriterNetworkSink::GetMaximumClients</a>