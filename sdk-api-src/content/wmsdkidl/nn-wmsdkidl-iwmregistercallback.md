---
UID: NN:wmsdkidl.IWMRegisterCallback
title: IWMRegisterCallback (wmsdkidl.h)
description: The IWMRegisterCallback interface enables the application to get status messages from a sink object.By default, the writer object does not send the application any status messages from the sink object.
helpviewer_keywords: ["IWMRegisterCallback","IWMRegisterCallback interface [windows Media Format]","IWMRegisterCallback interface [windows Media Format]","described","IWMRegisterCallbackInterface","wmformat.iwmregistercallback","wmsdkidl/IWMRegisterCallback"]
old-location: wmformat\iwmregistercallback.htm
tech.root: wmformat
ms.assetid: 3831b727-7fdc-4d05-a7b3-86ca5b5c3b17
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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
