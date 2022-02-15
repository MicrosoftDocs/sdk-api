---
UID: NN:wmsdkidl.IWMClientConnections
title: IWMClientConnections (wmsdkidl.h)
description: The IWMClientConnections interface manages the collecting of information about clients connected to a writer network sink object.The writer network sink object exposes this interface.
helpviewer_keywords: ["IWMClientConnections","IWMClientConnections interface [windows Media Format]","IWMClientConnections interface [windows Media Format]","described","IWMClientConnectionsInterface","wmformat.iwmclientconnections","wmsdkidl/IWMClientConnections"]
old-location: wmformat\iwmclientconnections.htm
tech.root: wmformat
ms.assetid: fea7cd85-22ab-4f3b-8a0a-301496f0c788
ms.date: 12/05/2018
ms.keywords: IWMClientConnections, IWMClientConnections interface [windows Media Format], IWMClientConnections interface [windows Media Format],described, IWMClientConnectionsInterface, wmformat.iwmclientconnections, wmsdkidl/IWMClientConnections
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
 - IWMClientConnections
 - wmsdkidl/IWMClientConnections
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
 - IWMClientConnections
---

# IWMClientConnections interface


## -description

The <b>IWMClientConnections</b> interface manages the collecting of information about clients connected to a writer network sink object.

The writer network sink object exposes this interface. You can retrieve a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface on a writer network sink object.

## -inheritance

The <b>IWMClientConnections</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMClientConnections</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2">IWMClientConnections2 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-network-sink-object">Writer Network Sink Object</a>
