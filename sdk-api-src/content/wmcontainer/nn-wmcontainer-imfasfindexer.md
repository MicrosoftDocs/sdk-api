---
UID: NN:wmcontainer.IMFASFIndexer
title: IMFASFIndexer (wmcontainer.h)
description: Provides methods to work with indexes in Systems Format (ASF) files.
helpviewer_keywords: ["93127fe4-bca9-4674-ae21-012367d7dd2f","IMFASFIndexer","IMFASFIndexer interface [Media Foundation]","IMFASFIndexer interface [Media Foundation]","described","mf.imfasfindexer","wmcontainer/IMFASFIndexer"]
old-location: mf\imfasfindexer.htm
tech.root: mf
ms.assetid: 93127fe4-bca9-4674-ae21-012367d7dd2f
ms.date: 12/05/2018
ms.keywords: 93127fe4-bca9-4674-ae21-012367d7dd2f, IMFASFIndexer, IMFASFIndexer interface [Media Foundation], IMFASFIndexer interface [Media Foundation],described, mf.imfasfindexer, wmcontainer/IMFASFIndexer
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFIndexer
 - wmcontainer/IMFASFIndexer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFIndexer
---

# IMFASFIndexer interface


## -description

Provides methods to work with indexes in Systems Format (ASF) files. The ASF indexer object exposes this interface. To create the ASF indexer, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer">MFCreateASFIndexer</a>.

## -inheritance

The <b>IMFASFIndexer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFIndexer</b> also has these types of members:

## -remarks

You can use the indexer object to read an existing ASF index or write a new index. The index object has two mutually exclusive modes: read mode and write mode. To set the mode, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags">SetFlags</a>. 

Use the following methods to configure the indexer object  (both modes):

<ul>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize">Initialize</a>
</li>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags">SetFlags</a>
</li>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams">SetIndexByteStreams</a>
</li>
</ul>
Use the following methods to read an existing index:

<ul>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getflags">GetFlags</a>
</li>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexbytestreamcount">GetIndexByteStreamCount</a>
</li>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition">GetIndexPosition</a>
</li>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus">GetIndexStatus</a>
</li>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue">GetSeekPositionForValue</a>
</li>
</ul>
Use the following methods to write an index:

<ul>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex">CommitIndex</a>
</li>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries">GenerateIndexEntries</a>
</li>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex">GetCompletedIndex</a>
</li>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace">GetIndexWriteSpace</a>
</li>
<li>
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus">SetIndexStatus</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer">MFCreateASFIndexer</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
