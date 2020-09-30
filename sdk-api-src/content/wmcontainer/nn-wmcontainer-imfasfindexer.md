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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFIndexer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFIndexer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFIndexer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex">CommitIndex</a>
</td>
<td align="left" width="63%">
Adds information about  new index entries to the <a href="/windows/desktop/medfound/asf-contentinfo-object">ContentInfo</a> object of the output file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries">GenerateIndexEntries</a>
</td>
<td align="left" width="63%">
Creates index entries for the specified ASF data packet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex">GetCompletedIndex</a>
</td>
<td align="left" width="63%">
Retrieves the completed index from the ASF indexer object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves the flags that indicate the selected indexer options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexbytestreamcount">GetIndexByteStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of byte streams that are included in the index. This method currently only retrieves 1.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition">GetIndexPosition</a>
</td>
<td align="left" width="63%">
Retrieves the offset of the ASF Index Object relative to start of the ASF file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus">GetIndexStatus</a>
</td>
<td align="left" width="63%">
Retrieves the index settings for a specified stream and index type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace">GetIndexWriteSpace</a>
</td>
<td align="left" width="63%">
Retrieves the size of the buffer required to store the completed index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue">GetSeekPositionForValue</a>
</td>
<td align="left" width="63%">
Given a desired seek time, retrieves the offset from which the client should start reading data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the indexer with the <a href="/windows/desktop/medfound/asf-contentinfo-object">ContentInfo</a> object of the ASF file to be read or encoded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Specifies the read or the write mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams">SetIndexByteStreams</a>
</td>
<td align="left" width="63%">
Sets the byte stream that contains the index entries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus">SetIndexStatus</a>
</td>
<td align="left" width="63%">
Specifies the type of index entries that the indexer must generate for the ASF file.


</td>
</tr>
</table>

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