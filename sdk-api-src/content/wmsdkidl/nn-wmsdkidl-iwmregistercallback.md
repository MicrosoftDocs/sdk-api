---
UID: NN:wmsdkidl.IWMRegisterCallback
title: IWMRegisterCallback (wmsdkidl.h)
description: The IWMRegisterCallback interface enables the application to get status messages from a sink object.By default, the writer object does not send the application any status messages from the sink object.
helpviewer_keywords: ["IWMRegisterCallback","IWMRegisterCallback interface [windows Media Format]","IWMRegisterCallback interface [windows Media Format]","described","IWMRegisterCallbackInterface","wmformat.iwmregistercallback","wmsdkidl/IWMRegisterCallback"]
old-location: wmformat\iwmregistercallback.htm
tech.root: wmformat
ms.assetid: 3831b727-7fdc-4d05-a7b3-86ca5b5c3b17
ms.date: 12/05/2018
ms.keywords: IWMRegisterCallback, IWMRegisterCallback interface [windows Media Format], IWMRegisterCallback interface [windows Media Format],described, IWMRegisterCallbackInterface, wmformat.iwmregistercallback, wmsdkidl/IWMRegisterCallback
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
 - IWMRegisterCallback
 - wmsdkidl/IWMRegisterCallback
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
 - IWMRegisterCallback
---

# IWMRegisterCallback interface


## -description

The <b>IWMRegisterCallback</b> interface enables the application to get status messages from a sink object.

By default, the writer object does not send the application any status messages from the sink object. To get status messages from a sink object, the application must query the sink object for the <b>IWMRegisterCallback</b> interface and call the <b>Advise</b> method.

The file sink object, the network sink object, and the push sink object all expose this interface. To obtain a pointer to this interface for a sink, call <b>QueryInterface</b> on any of these sink objects.

## -inheritance

The <b>IWMRegisterCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMRegisterCallback</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-file-sink-object">Writer File Sink Object</a>



<a href="/windows/desktop/wmformat/writer-network-sink-object">Writer Network Sink Object</a>
