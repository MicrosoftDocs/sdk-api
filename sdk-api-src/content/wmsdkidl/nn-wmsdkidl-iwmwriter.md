---
UID: NN:wmsdkidl.IWMWriter
title: IWMWriter (wmsdkidl.h)
description: The IWMWriter interface is used to write ASF files.
helpviewer_keywords: ["IWMWriter","IWMWriter interface [windows Media Format]","IWMWriter interface [windows Media Format]","described","IWMWriterInterface","wmformat.iwmwriter","wmsdkidl/IWMWriter"]
old-location: wmformat\iwmwriter.htm
tech.root: wmformat
ms.assetid: a194ef11-5203-4e85-af91-cdce0c53fe76
ms.date: 4/26/2023
ms.keywords: IWMWriter, IWMWriter interface [windows Media Format], IWMWriter interface [windows Media Format],described, IWMWriterInterface, wmformat.iwmwriter, wmsdkidl/IWMWriter
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
 - IWMWriter
 - wmsdkidl/IWMWriter
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
 - IWMWriter
---

# IWMWriter interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMWriter</b> interface is used to write ASF files. It includes methods for allocating buffers, setting and retrieving input properties, and setting profiles and output file names. The writer object exposes this interface. To create the writer object, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriter">WMCreateWriter</a> function.

## -inheritance

The <b>IWMWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWriter</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink">IWMWriterFileSink Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink">IWMWriterNetworkSink Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>



<a href="/windows/desktop/wmformat/writing-asf-files">Writing ASF Files</a>
