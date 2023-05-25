---
UID: NN:wmsdkidl.IWMWriterPreprocess
title: IWMWriterPreprocess (wmsdkidl.h)
description: The IWMWriterPreprocess interface handles multi-pass encoding.
helpviewer_keywords: ["IWMWriterPreprocess","IWMWriterPreprocess interface [windows Media Format]","IWMWriterPreprocess interface [windows Media Format]","described","IWMWriterPreprocessInterface","wmformat.iwmwriterpreprocess","wmsdkidl/IWMWriterPreprocess"]
old-location: wmformat\iwmwriterpreprocess.htm
tech.root: wmformat
ms.assetid: 06803639-3f21-4003-a460-16a0b5cc6d6f
ms.date: 4/26/2023
ms.keywords: IWMWriterPreprocess, IWMWriterPreprocess interface [windows Media Format], IWMWriterPreprocess interface [windows Media Format],described, IWMWriterPreprocessInterface, wmformat.iwmwriterpreprocess, wmsdkidl/IWMWriterPreprocess
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
 - IWMWriterPreprocess
 - wmsdkidl/IWMWriterPreprocess
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
 - IWMWriterPreprocess
---

# IWMWriterPreprocess interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMWriterPreprocess</b> interface handles multi-pass encoding. By making more than one pass, the writer can obtain better quality with better compression.

An <b>IWMWriterPreprocess</b> interface exists for every instance of the writer object. You can obtain a pointer to <b>IWMWriterPreprocess</b> with a call to the <b>QueryInterface</b> method of any other interface in the writer object.

## -inheritance

The <b>IWMWriterPreprocess</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMWriterPreprocess</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/using-two-pass-encoding">Using Two-Pass Encoding</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
