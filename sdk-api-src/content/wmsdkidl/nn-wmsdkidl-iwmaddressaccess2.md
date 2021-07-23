---
UID: NN:wmsdkidl.IWMAddressAccess2
title: IWMAddressAccess2 (wmsdkidl.h)
description: The IWMAddressAccess2 interface controls IP access lists on the writer network sink object.
helpviewer_keywords: ["IWMAddressAccess2","IWMAddressAccess2 interface [windows Media Format]","IWMAddressAccess2 interface [windows Media Format]","described","IWMAddressAccess2Interface","wmformat.iwmaddressaccess2","wmsdkidl/IWMAddressAccess2"]
old-location: wmformat\iwmaddressaccess2.htm
tech.root: wmformat
ms.assetid: 609a20a7-e1a3-4889-abf3-4a6defc7739a
ms.date: 12/05/2018
ms.keywords: IWMAddressAccess2, IWMAddressAccess2 interface [windows Media Format], IWMAddressAccess2 interface [windows Media Format],described, IWMAddressAccess2Interface, wmformat.iwmaddressaccess2, wmsdkidl/IWMAddressAccess2
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
 - IWMAddressAccess2
 - wmsdkidl/IWMAddressAccess2
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
 - IWMAddressAccess2
---

# IWMAddressAccess2 interface


## -description

The <b>IWMAddressAccess2</b> interface controls IP access lists on the writer network sink object. Applications can use this interface to exclude specific IP addresses, or ranges of IP addresses, from connecting to the network sink. To obtain this interface, call <b>QueryInterface</b> on another interface of the writer network sink object.

This interface extends the <b>IWMAddressAccess</b> interface by adding support for Internet Protocol version 6 (IPv6) addresses.



The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess">IWMAddressAccess</a>
</td>
<td> IID_IWMAddressAccess </td>
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

The <b>IWMAddressAccess2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess">IWMAddressAccess</a>. <b>IWMAddressAccess2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess">IWMAddressAccess</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-network-sink-object">Writer Network Sink Object</a>
