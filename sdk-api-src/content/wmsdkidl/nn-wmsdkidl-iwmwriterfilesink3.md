---
UID: NN:wmsdkidl.IWMWriterFileSink3
title: IWMWriterFileSink3 (wmsdkidl.h)
description: The IWMWriterFileSink3 interface provides additional functionality to the file sink object. To obtain a pointer to this interface, call QueryInterface on the file sink object.
helpviewer_keywords: ["IWMWriterFileSink3","IWMWriterFileSink3 interface [windows Media Format]","IWMWriterFileSink3 interface [windows Media Format]","described","IWMWriterFileSink3Interface","wmformat.iwmwriterfilesink3","wmsdkidl/IWMWriterFileSink3"]
old-location: wmformat\iwmwriterfilesink3.htm
tech.root: wmformat
ms.assetid: 67f418c8-184d-46f0-8939-69194c7e7a50
ms.date: 4/26/2023
ms.keywords: IWMWriterFileSink3, IWMWriterFileSink3 interface [windows Media Format], IWMWriterFileSink3 interface [windows Media Format],described, IWMWriterFileSink3Interface, wmformat.iwmwriterfilesink3, wmsdkidl/IWMWriterFileSink3
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
 - IWMWriterFileSink3
 - wmsdkidl/IWMWriterFileSink3
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
 - IWMWriterFileSink3
---

# IWMWriterFileSink3 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMWriterFileSink3</b> interface provides additional functionality to the file sink object. To obtain a pointer to this interface, call <b>QueryInterface</b> on the file sink object.

## -inheritance

The <b>IWMWriterFileSink3</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2</a>. <b>IWMWriterFileSink3</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink">IWMWriterFileSink Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>



<a href="/windows/desktop/wmformat/using-file-sinks">Using File Sinks</a>



<a href="/windows/desktop/wmformat/writer-file-sink-object">Writer File Sink Object</a>
