---
UID: NN:wmsdkidl.IWMClientConnections2
title: IWMClientConnections2 (wmsdkidl.h)
description: The IWMClientConnections2 interface retrieves advanced client information.The writer network sink object exposes this interface.
helpviewer_keywords: ["IWMClientConnections2","IWMClientConnections2 interface [windows Media Format]","IWMClientConnections2 interface [windows Media Format]","described","IWMClientConnections2Interface","wmformat.iwmclientconnections2","wmsdkidl/IWMClientConnections2"]
old-location: wmformat\iwmclientconnections2.htm
tech.root: wmformat
ms.assetid: 7148dd13-e5de-4adb-89e7-3f02a463c2d1
ms.date: 12/05/2018
ms.keywords: IWMClientConnections2, IWMClientConnections2 interface [windows Media Format], IWMClientConnections2 interface [windows Media Format],described, IWMClientConnections2Interface, wmformat.iwmclientconnections2, wmsdkidl/IWMClientConnections2
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
 - IWMClientConnections2
 - wmsdkidl/IWMClientConnections2
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
 - IWMClientConnections2
---

# IWMClientConnections2 interface


## -description

The <b>IWMClientConnections2</b> interface retrieves advanced client information.

The writer network sink object exposes this interface. You can retrieve a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface on a writer network sink object.



The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections">IWMClientConnections</a>
</td>
<td>IID_IWMClientConnections</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback">IWMRegisterCallback</a>
</td>
<td>IID_IWMRegisterCallback</td>
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

The <b>IWMClientConnections2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections">IWMClientConnections</a>. <b>IWMClientConnections2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections">IWMClientConnections</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
