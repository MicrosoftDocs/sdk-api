---
UID: NN:wmsdkidl.IWMHeaderInfo2
title: IWMHeaderInfo2 (wmsdkidl.h)
description: The IWMHeaderInfo2 interface exposes information about the codecs used to create the content in a file.The IWMHeaderInfo2 interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object.
helpviewer_keywords: ["IWMHeaderInfo2","IWMHeaderInfo2 interface [windows Media Format]","IWMHeaderInfo2 interface [windows Media Format]","described","IWMHeaderInfo2Interface","wmformat.iwmheaderinfo2","wmsdkidl/IWMHeaderInfo2"]
old-location: wmformat\iwmheaderinfo2.htm
tech.root: wmformat
ms.assetid: af670b54-f695-4b6f-8190-c25ea409b53a
ms.date: 4/26/2023
ms.keywords: IWMHeaderInfo2, IWMHeaderInfo2 interface [windows Media Format], IWMHeaderInfo2 interface [windows Media Format],described, IWMHeaderInfo2Interface, wmformat.iwmheaderinfo2, wmsdkidl/IWMHeaderInfo2
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
 - IWMHeaderInfo2
 - wmsdkidl/IWMHeaderInfo2
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
 - IWMHeaderInfo2
---

# IWMHeaderInfo2 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMHeaderInfo2</b> interface exposes information about the <a href="/windows/desktop/wmformat/wmformat-glossary">codecs</a> used to create the content in a file.

The <b>IWMHeaderInfo2</b> interface is implemented by the metadata editor object, the writer object, the reader object, and the synchronous reader object. To obtain a pointer to an instance, call the <b>QueryInterface</b> method of any other interface in the desired object.

## -inheritance

The <b>IWMHeaderInfo2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo</a>. <b>IWMHeaderInfo2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

For information about using the writer for metadata editing, see <a href="/windows/desktop/wmformat/to-edit-metadata-with-the-writer">To Edit Metadata with the Writer</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
