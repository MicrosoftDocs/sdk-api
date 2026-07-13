---
UID: NN:wmsdkidl.IWMWriterSink
title: IWMWriterSink (wmsdkidl.h)
description: The IWMWriterSink interface is the basic interface of all writer sinks, including the file, network, and push sinks defined in the Windows Media Format SDK, and custom sinks.
helpviewer_keywords: ["IWMWriterSink","IWMWriterSink interface [windows Media Format]","IWMWriterSink interface [windows Media Format]","described","IWMWriterSinkInterface","wmformat.iwmwritersink","wmsdkidl/IWMWriterSink"]
old-location: wmformat\iwmwritersink.htm
tech.root: wmformat
ms.assetid: 73656814-7fac-4567-abcd-dbb3243fcaa8
ms.date: 4/26/2023
ms.keywords: IWMWriterSink, IWMWriterSink interface [windows Media Format], IWMWriterSink interface [windows Media Format],described, IWMWriterSinkInterface, wmformat.iwmwritersink, wmsdkidl/IWMWriterSink
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
 - IWMWriterSink
 - wmsdkidl/IWMWriterSink
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
 - IWMWriterSink
---

# IWMWriterSink interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMWriterSink</b> interface is the basic interface of all writer sinks, including the file, network, and push sinks defined in the Windows Media Format SDK, and custom sinks. If you are using one of the defined writer sinks, you never need to deal with the methods of this interface. If you are creating your own custom writer sink, you must implement these methods in your application.

This interface exists on the writer file sink object, the writer network sink object, and the writer push sink object. You should never obtain a pointer to this interface from one of these objects, however, as its methods are called internally by the writer sink objects and the writer object. You can create a class in your application that inherits from this interface to make your own sink.

## -inheritance

The <b>IWMWriterSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWriterSink</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-file-sink-object">Writer File Sink Object</a>



<a href="/windows/desktop/wmformat/writer-network-sink-object">Writer Network Sink Object</a>



<a href="/windows/desktop/wmformat/writer-push-sink-object">Writer Push Sink Object</a>
