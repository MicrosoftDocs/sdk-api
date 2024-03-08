---
UID: NN:wmsdkidl.IWMSyncReader
title: IWMSyncReader (wmsdkidl.h)
description: The IWMSyncReader interface provides the ability to read ASF files using synchronous calls.
helpviewer_keywords: ["IWMSyncReader","IWMSyncReader interface [windows Media Format]","IWMSyncReader interface [windows Media Format]","described","IWMSyncReaderInterface","wmformat.iwmsyncreader","wmsdkidl/IWMSyncReader"]
old-location: wmformat\iwmsyncreader.htm
tech.root: wmformat
ms.assetid: 2a46e79f-084e-4173-ad0f-211d3065d81a
ms.date: 4/26/2023
ms.keywords: IWMSyncReader, IWMSyncReader interface [windows Media Format], IWMSyncReader interface [windows Media Format],described, IWMSyncReaderInterface, wmformat.iwmsyncreader, wmsdkidl/IWMSyncReader
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
 - IWMSyncReader
 - wmsdkidl/IWMSyncReader
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
 - IWMSyncReader
---

# IWMSyncReader interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMSyncReader</b> interface provides the ability to read ASF files using synchronous calls. This is in contrast to many of the methods in <b>IWMReader</b>, which are called asynchronously.

You get a pointer to an <b>IWMSyncReader</b> interface when you create a new synchronous reader object with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatesyncreader">WMCreateSyncReader</a>.

In addition to enabling synchronous reading, the methods of <b>IWMSyncReader</b> are tailored to meet the demands of editing applications. Default playback from <b>IWMSyncReader</b> delivers uncompressed samples for the default streams of all outputs. However, you can manipulate the selected streams during streaming without having to enable manual stream selection. You can also receive compressed or uncompressed samples, though you cannot change between them during streaming. Samples are delivered by either output number or stream number, so you can receive uncompressed samples from mutually exclusive streams.

Many of the methods in this interface are almost identical to corresponding methods in the asynchronous reader.

Use of this interface, as well as the implementation of an <b>IStream</b> COM object that passes data to this object, is demonstrated in the WMSyncReader SDK sample.

## -inheritance

The <b>IWMSyncReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMSyncReader</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
