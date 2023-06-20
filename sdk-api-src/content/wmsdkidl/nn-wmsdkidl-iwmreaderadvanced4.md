---
UID: NN:wmsdkidl.IWMReaderAdvanced4
title: IWMReaderAdvanced4 (wmsdkidl.h)
description: The IWMReaderAdvanced4 interface provides additional functionality to the reader.An IWMReaderAdvanced4 interface exists for every reader object.
helpviewer_keywords: ["IWMReaderAdvanced4","IWMReaderAdvanced4 interface [windows Media Format]","IWMReaderAdvanced4 interface [windows Media Format]","described","IWMReaderAdvanced4Interface","wmformat.iwmreaderadvanced4","wmsdkidl/IWMReaderAdvanced4"]
old-location: wmformat\iwmreaderadvanced4.htm
tech.root: wmformat
ms.assetid: 56695c57-f6c5-4c57-b3d4-73d169b379fa
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced4, IWMReaderAdvanced4 interface [windows Media Format], IWMReaderAdvanced4 interface [windows Media Format],described, IWMReaderAdvanced4Interface, wmformat.iwmreaderadvanced4, wmsdkidl/IWMReaderAdvanced4
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
 - IWMReaderAdvanced4
 - wmsdkidl/IWMReaderAdvanced4
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
 - IWMReaderAdvanced4
---

# IWMReaderAdvanced4 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMReaderAdvanced4</b> interface provides additional functionality to the reader.

An <b>IWMReaderAdvanced4</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface in the reader object.

## -inheritance

The <b>IWMReaderAdvanced4</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3</a>. <b>IWMReaderAdvanced4</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5">IWMReaderAdvanced5 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced6">IWMReaderAdvanced6 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="/windows/desktop/wmformat/reading-asf-files">Reading ASF Files</a>
