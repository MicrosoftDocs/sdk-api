---
UID: NN:wmsdkidl.IWMWriterNetworkSink
title: IWMWriterNetworkSink (wmsdkidl.h)
description: The IWMWriterNetworkSink interface is used to deliver streams to the network.
helpviewer_keywords: ["IWMWriterNetworkSink","IWMWriterNetworkSink interface [windows Media Format]","IWMWriterNetworkSink interface [windows Media Format]","described","IWMWriterNetworkSinkInterface","wmformat.iwmwriternetworksink","wmsdkidl/IWMWriterNetworkSink"]
old-location: wmformat\iwmwriternetworksink.htm
tech.root: wmformat
ms.assetid: 3204c360-f407-4cf3-bb21-7e6094587fb0
ms.date: 12/05/2018
ms.keywords: IWMWriterNetworkSink, IWMWriterNetworkSink interface [windows Media Format], IWMWriterNetworkSink interface [windows Media Format],described, IWMWriterNetworkSinkInterface, wmformat.iwmwriternetworksink, wmsdkidl/IWMWriterNetworkSink
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
 - IWMWriterNetworkSink
 - wmsdkidl/IWMWriterNetworkSink
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
 - IWMWriterNetworkSink
---

# IWMWriterNetworkSink interface


## -description

The <b>IWMWriterNetworkSink</b> interface is used to deliver streams to the network. It inherits all the methods of <b>IWMWriterSink</b>, and adds methods to configure the network sink.

The network sink object exposes this interface. To create the network sink object, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink">WMCreateWriterNetworkSink</a> function.

## -inheritance

The <b>IWMWriterNetworkSink</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>. <b>IWMWriterNetworkSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/broadcasting-asf-data">Broadcasting ASF Data</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
