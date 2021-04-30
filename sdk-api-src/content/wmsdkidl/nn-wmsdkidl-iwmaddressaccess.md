---
UID: NN:wmsdkidl.IWMAddressAccess
title: IWMAddressAccess (wmsdkidl.h)
description: The IWMAddressAccess interface controls IP access lists on the writer network sink object.
helpviewer_keywords: ["IWMAddressAccess","IWMAddressAccess interface [windows Media Format]","IWMAddressAccess interface [windows Media Format]","described","IWMAddressAccessInterface","wmformat.iwmaddressaccess","wmsdkidl/IWMAddressAccess"]
old-location: wmformat\iwmaddressaccess.htm
tech.root: wmformat
ms.assetid: 7251c600-90a2-4903-b26a-643b4d10b0ce
ms.date: 12/05/2018
ms.keywords: IWMAddressAccess, IWMAddressAccess interface [windows Media Format], IWMAddressAccess interface [windows Media Format],described, IWMAddressAccessInterface, wmformat.iwmaddressaccess, wmsdkidl/IWMAddressAccess
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMAddressAccess
 - wmsdkidl/IWMAddressAccess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMAddressAccess
---

# IWMAddressAccess interface


## -description

The <b>IWMAddressAccess</b> interface controls IP access lists on the writer network sink object. Applications can use this interface to exclude specific IP addresses, or ranges of IP addresses, from connecting to the network sink. To obtain this interface, call <b>QueryInterface</b> on another interface of the writer network sink object.

This interface supports only Internet Protocol version 4 (IPv4) addresses. The <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess2">IWMAddressAccess2</a> interface inherits <b>IWMAddressAccess</b> and adds support for IPv6 addresses.



The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess2">IWMAddressAccess2</a>
</td>
<td> IID_IWMAddressAccess2 </td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections">IWMClientConnections</a>
</td>
<td>IID_IWMClientConnections</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2">IWMClientConnections2</a>
</td>
<td>IID_IWMClientConnections2</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink">IWMWriterNetworkSink</a>
</td>
<td>IID_IWMWriterNetworkSink</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMAddressAccess</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMAddressAccess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-network-sink-object">Writer Network Sink Object</a>
