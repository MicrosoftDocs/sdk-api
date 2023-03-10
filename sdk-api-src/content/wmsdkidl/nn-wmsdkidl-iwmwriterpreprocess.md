---
UID: NN:wmsdkidl.IWMWriterPreprocess
title: IWMWriterPreprocess (wmsdkidl.h)
description: The IWMWriterPreprocess interface handles multi-pass encoding.
helpviewer_keywords: ["IWMWriterPreprocess","IWMWriterPreprocess interface [windows Media Format]","IWMWriterPreprocess interface [windows Media Format]","described","IWMWriterPreprocessInterface","wmformat.iwmwriterpreprocess","wmsdkidl/IWMWriterPreprocess"]
old-location: wmformat\iwmwriterpreprocess.htm
tech.root: wmformat
ms.assetid: 06803639-3f21-4003-a460-16a0b5cc6d6f
ms.date: 12/05/2018
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
