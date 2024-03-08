---
UID: NN:wmsdkidl.IWMIndexer
title: IWMIndexer (wmsdkidl.h)
description: The IWMIndexer interface is used to create an index for ASF files to enable seeking.
helpviewer_keywords: ["IWMIndexer","IWMIndexer interface [windows Media Format]","IWMIndexer interface [windows Media Format]","described","IWMIndexerInterface","wmformat.iwmindexer","wmsdkidl/IWMIndexer"]
old-location: wmformat\iwmindexer.htm
tech.root: wmformat
ms.assetid: 00627b0c-4484-417a-8680-0fd97aac41fe
ms.date: 4/26/2023
ms.keywords: IWMIndexer, IWMIndexer interface [windows Media Format], IWMIndexer interface [windows Media Format],described, IWMIndexerInterface, wmformat.iwmindexer, wmsdkidl/IWMIndexer
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
 - IWMIndexer
 - wmsdkidl/IWMIndexer
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
 - IWMIndexer
---

# IWMIndexer interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMIndexer</b> interface is used to create an index for ASF files to enable seeking. An index is created only for a file that contains video, although the indexer can safely be used on files that do not contain any video.

An index is an object in the ASF file that equates video samples with presentation times. This is important because the timing of video frames is not necessarily easily computed from the <a href="/windows/desktop/wmformat/wmformat-glossary">frame rate</a>.

In addition to the standard temporal index, the indexer object can create indexes based on video frame number and SMPTE time code. For more information about creating these indexes, see <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer2-configure">IWMIndexer2::Configure</a>.

This interface can be obtained by using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreateindexer">WMCreateIndexer</a> function.

## -inheritance

The <b>IWMIndexer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMIndexer</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/indexer-object">Indexer Object</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
