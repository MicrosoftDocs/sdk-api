---
UID: NN:wmsdkidl.IWMReaderTimecode
title: IWMReaderTimecode (wmsdkidl.h)
description: The IWMReaderTimecode interface provides access to information about SMPTE (Society of Motion Picture and Television Engineers) time code ranges.
helpviewer_keywords: ["IWMReaderTimecode","IWMReaderTimecode interface [windows Media Format]","IWMReaderTimecode interface [windows Media Format]","described","IWMReaderTimecodeInterface","wmformat.iwmreadertimecode","wmsdkidl/IWMReaderTimecode"]
old-location: wmformat\iwmreadertimecode.htm
tech.root: wmformat
ms.assetid: 7f7d5608-c505-46ab-9e1e-e45b383c879b
ms.date: 4/26/2023
ms.keywords: IWMReaderTimecode, IWMReaderTimecode interface [windows Media Format], IWMReaderTimecode interface [windows Media Format],described, IWMReaderTimecodeInterface, wmformat.iwmreadertimecode, wmsdkidl/IWMReaderTimecode
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
 - IWMReaderTimecode
 - wmsdkidl/IWMReaderTimecode
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
 - IWMReaderTimecode
---

# IWMReaderTimecode interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMReaderTimecode</b> interface provides access to information about SMPTE (Society of Motion Picture and Television Engineers) time code ranges. A range of SMPTE time code is a series of samples with time codes that are contiguous and in increasing order. An individual video stream can contain more than one range.

An <b>IWMReaderTimecode</b> interface exists for every reader object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any other interface of the reader object.

## -inheritance

The <b>IWMReaderTimecode</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderTimecode</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>
