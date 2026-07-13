---
UID: NN:wmsdkidl.IWMWriterPushSink
title: IWMWriterPushSink (wmsdkidl.h)
description: The IWMWriterPushSink interface enables the application to send ASF files to a publishing point on a Windows Media server.
helpviewer_keywords: ["IWMWriterPushSink","IWMWriterPushSink interface [windows Media Format]","IWMWriterPushSink interface [windows Media Format]","described","IWMWriterPushSinkInterface","wmformat.iwmwriterpushsink","wmsdkidl/IWMWriterPushSink"]
old-location: wmformat\iwmwriterpushsink.htm
tech.root: wmformat
ms.assetid: 47bee154-0d29-4f4c-ac38-af8747088024
ms.date: 4/26/2023
ms.keywords: IWMWriterPushSink, IWMWriterPushSink interface [windows Media Format], IWMWriterPushSink interface [windows Media Format],described, IWMWriterPushSinkInterface, wmformat.iwmwriterpushsink, wmsdkidl/IWMWriterPushSink
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
 - IWMWriterPushSink
 - wmsdkidl/IWMWriterPushSink
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
 - IWMWriterPushSink
---

# IWMWriterPushSink interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMWriterPushSink</b> interface enables the application to send ASF files to a publishing point on a Windows Media server. The writer push sink object exposes this interface. To create an instance of the writer push sink, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink">WMCreateWriterPushSink</a> function.

## -inheritance

The <b>IWMWriterPushSink</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>. <b>IWMWriterPushSink</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/sending-asf-data-to-a-publishing-point">Sending ASF Data to a Publishing Point</a>



<a href="/windows/desktop/wmformat/writer-push-sink-object">Writer Push Sink Object</a>
