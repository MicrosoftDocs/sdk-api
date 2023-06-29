---
UID: NN:wmsdkidl.IWMIndexer2
title: IWMIndexer2 (wmsdkidl.h)
description: The IWMIndexer2 interface enables you to change the settings of the indexer object to suit your needs.This interface is implemented as part of the indexer object.
helpviewer_keywords: ["IWMIndexer2","IWMIndexer2 interface [windows Media Format]","IWMIndexer2 interface [windows Media Format]","described","IWMIndexer2Interface","wmformat.iwmindexer2","wmsdkidl/IWMIndexer2"]
old-location: wmformat\iwmindexer2.htm
tech.root: wmformat
ms.assetid: ce900a2b-765b-46bb-87f4-bf9fe57d1cdb
ms.date: 4/26/2023
ms.keywords: IWMIndexer2, IWMIndexer2 interface [windows Media Format], IWMIndexer2 interface [windows Media Format],described, IWMIndexer2Interface, wmformat.iwmindexer2, wmsdkidl/IWMIndexer2
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
 - IWMIndexer2
 - wmsdkidl/IWMIndexer2
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
 - IWMIndexer2
---

# IWMIndexer2 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMIndexer2</b> interface enables you to change the settings of the indexer object to suit your needs.

This interface is implemented as part of the indexer object. To obtain a pointer to <b>IWMIndexer2</b>, call the <b>QueryInterface</b> method of the <b>IWMIndexer</b> interface.

## -inheritance

The <b>IWMIndexer2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer">IWMIndexer</a>. <b>IWMIndexer2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer">IWMIndexer Interface</a>



<a href="/windows/desktop/wmformat/indexer-object">Indexer Object</a>
