---
UID: NF:wmsdkidl.IWMClientConnections.GetClientCount
title: IWMClientConnections::GetClientCount (wmsdkidl.h)
description: The GetClientCount method retrieves the number of connected clients.
helpviewer_keywords: ["GetClientCount","GetClientCount method [windows Media Format]","GetClientCount method [windows Media Format]","IWMClientConnections interface","IWMClientConnections interface [windows Media Format]","GetClientCount method","IWMClientConnections.GetClientCount","IWMClientConnections::GetClientCount","IWMClientConnectionsGetClientCount","wmformat.iwmclientconnections_getclientcount","wmsdkidl/IWMClientConnections::GetClientCount"]
old-location: wmformat\iwmclientconnections_getclientcount.htm
tech.root: wmformat
ms.assetid: 208b40cd-c138-4311-8702-18a61713b71a
ms.date: 4/26/2023
ms.keywords: GetClientCount, GetClientCount method [windows Media Format], GetClientCount method [windows Media Format],IWMClientConnections interface, IWMClientConnections interface [windows Media Format],GetClientCount method, IWMClientConnections.GetClientCount, IWMClientConnections::GetClientCount, IWMClientConnectionsGetClientCount, wmformat.iwmclientconnections_getclientcount, wmsdkidl/IWMClientConnections::GetClientCount
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
 - IWMClientConnections::GetClientCount
 - wmsdkidl/IWMClientConnections::GetClientCount
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
 - IWMClientConnections.GetClientCount
---

# IWMClientConnections::GetClientCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetClientCount</b> method retrieves the number of connected clients.

## -parameters

### -param pcClients [out]

Pointer to a count of the clients that are connected.

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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Streaming has not yet begun.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pcClients</i> has been passed a null value.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections">IWMClientConnections Interface</a>