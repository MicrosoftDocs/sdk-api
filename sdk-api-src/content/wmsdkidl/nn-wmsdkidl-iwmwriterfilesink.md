---
UID: NN:wmsdkidl.IWMWriterFileSink
title: IWMWriterFileSink (wmsdkidl.h)
description: The IWMWriterFileSink interface is used to open a file to which the writer can write data. The file sink object exposes this interface. To create the file sink object, call the WMCreateWriterFileSink function.
helpviewer_keywords: ["IWMWriterFileSink","IWMWriterFileSink interface [windows Media Format]","IWMWriterFileSink interface [windows Media Format]","described","IWMWriterFileSinkInterface","wmformat.iwmwriterfilesink","wmsdkidl/IWMWriterFileSink"]
old-location: wmformat\iwmwriterfilesink.htm
tech.root: wmformat
ms.assetid: af47b130-353e-411d-8432-09ecd20a70d2
ms.date: 4/26/2023
ms.keywords: IWMWriterFileSink, IWMWriterFileSink interface [windows Media Format], IWMWriterFileSink interface [windows Media Format],described, IWMWriterFileSinkInterface, wmformat.iwmwriterfilesink, wmsdkidl/IWMWriterFileSink
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
 - IWMWriterFileSink
 - wmsdkidl/IWMWriterFileSink
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
 - IWMWriterFileSink
---

# IWMWriterFileSink interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMWriterFileSink</b> interface is used to open a file to which the writer can write data. The file sink object exposes this interface. To create the file sink object, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink">WMCreateWriterFileSink</a> function.

## -inheritance

The <b>IWMWriterFileSink</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>. <b>IWMWriterFileSink</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3">IWMWriterFileSink3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/using-file-sinks">Using File Sinks</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
