---
UID: NF:wmsdkidl.IWMClientConnections.GetClientProperties
title: IWMClientConnections::GetClientProperties (wmsdkidl.h)
description: The GetClientProperties method retrieves information, including the IP address and protocol, about a connected client.
helpviewer_keywords: ["GetClientProperties","GetClientProperties method [windows Media Format]","GetClientProperties method [windows Media Format]","IWMClientConnections interface","IWMClientConnections interface [windows Media Format]","GetClientProperties method","IWMClientConnections.GetClientProperties","IWMClientConnections::GetClientProperties","IWMClientConnectionsGetClientProperties","wmformat.iwmclientconnections_getclientproperties","wmsdkidl/IWMClientConnections::GetClientProperties"]
old-location: wmformat\iwmclientconnections_getclientproperties.htm
tech.root: wmformat
ms.assetid: a05d7d1e-21dc-4e2a-a17b-5f04e639b143
ms.date: 12/05/2018
ms.keywords: GetClientProperties, GetClientProperties method [windows Media Format], GetClientProperties method [windows Media Format],IWMClientConnections interface, IWMClientConnections interface [windows Media Format],GetClientProperties method, IWMClientConnections.GetClientProperties, IWMClientConnections::GetClientProperties, IWMClientConnectionsGetClientProperties, wmformat.iwmclientconnections_getclientproperties, wmsdkidl/IWMClientConnections::GetClientProperties
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
 - IWMClientConnections::GetClientProperties
 - wmsdkidl/IWMClientConnections::GetClientProperties
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
 - IWMClientConnections.GetClientProperties
---

# IWMClientConnections::GetClientProperties


## -description

The <b>GetClientProperties</b> method retrieves information, including the IP address and protocol, about a connected client.

## -parameters

### -param dwClientNum [in]

<b>DWORD</b> containing the client's index number.

### -param pClientProperties [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties">WM_CLIENT_PROPERTIES</a> structure.

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
<i>pcClientProperties</i> has been passed a null value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
A client number larger than the number of clients has been passed in.

OR

Failed to get client information for unspecified reason.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections">IWMClientConnections Interface</a>