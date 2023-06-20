---
UID: NN:wmsdkidl.IWMReaderAdvanced3
title: IWMReaderAdvanced3 (wmsdkidl.h)
description: The IWMReaderAdvanced3 interface provides additional functionality to the reader object.
helpviewer_keywords: ["IWMReaderAdvanced3","IWMReaderAdvanced3 interface [windows Media Format]","IWMReaderAdvanced3 interface [windows Media Format]","described","IWMReaderAdvanced3Interface","wmformat.iwmreaderadvanced3","wmsdkidl/IWMReaderAdvanced3"]
old-location: wmformat\iwmreaderadvanced3.htm
tech.root: wmformat
ms.assetid: 20bf3c00-0f35-4b8e-b78d-a36fbfd865b7
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced3, IWMReaderAdvanced3 interface [windows Media Format], IWMReaderAdvanced3 interface [windows Media Format],described, IWMReaderAdvanced3Interface, wmformat.iwmreaderadvanced3, wmsdkidl/IWMReaderAdvanced3
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
 - IWMReaderAdvanced3
 - wmsdkidl/IWMReaderAdvanced3
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
 - IWMReaderAdvanced3
---

# IWMReaderAdvanced3 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMReaderAdvanced3</b> interface provides additional functionality to the reader object. It contains methods that enhance the ability to playback a file.

<b>IWMReaderAdvanced3</b> exists for each instance of the reader objects created with the <b>WMCreateReader</b> function.

## -inheritance

The <b>IWMReaderAdvanced3</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2</a>. <b>IWMReaderAdvanced3</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5">IWMReaderAdvanced5 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced6">IWMReaderAdvanced6 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="/windows/desktop/wmformat/reading-asf-files">Reading ASF Files</a>
