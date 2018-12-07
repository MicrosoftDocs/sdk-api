---
UID: NN:wmcontainer.IMFASFIndexer
title: IMFASFIndexer
author: windows-sdk-content
description: Provides methods to work with indexes in Systems Format (ASF) files.
old-location: mf\imfasfindexer.htm
tech.root: medfound
ms.assetid: 93127fe4-bca9-4674-ae21-012367d7dd2f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 93127fe4-bca9-4674-ae21-012367d7dd2f, IMFASFIndexer, IMFASFIndexer interface [Media Foundation], IMFASFIndexer interface [Media Foundation],described, mf.imfasfindexer, wmcontainer/IMFASFIndexer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFIndexer interface


## -description


Provides methods to work with indexes in Systems Format (ASF) files. The ASF indexer object exposes this interface. To create the ASF indexer, call <a href="https://msdn.microsoft.com/df141f8e-10b4-4ac4-8a83-c25764b8f0c6">MFCreateASFIndexer</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFIndexer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFASFIndexer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/44b889e1-8860-44fa-b19f-5be9f844a194">CommitIndex</a>
</td>
<td align="left" width="63%">
Adds information about  new index entries to the <a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ContentInfo</a> object of the output file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/febc5335-a8e8-4ae9-afb2-17f09b750477">GenerateIndexEntries</a>
</td>
<td align="left" width="63%">
Creates index entries for the specified ASF data packet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aca721e8-e610-4022-a3da-8ff5a5943e3e">GetCompletedIndex</a>
</td>
<td align="left" width="63%">
Retrieves the completed index from the ASF indexer object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97809620-57ad-48f1-94ba-a2e121cdfee6">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves the flags that indicate the selected indexer options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a433af8a-9e8a-4234-9694-c3a5420a1710">GetIndexByteStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of byte streams that are included in the index. This method currently only retrieves 1.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ef0e36c-1be5-44ac-8f6a-e29805c99e78">GetIndexPosition</a>
</td>
<td align="left" width="63%">
Retrieves the offset of the ASF Index Object relative to start of the ASF file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc38a060-36e4-458e-829e-2770387fc484">GetIndexStatus</a>
</td>
<td align="left" width="63%">
Retrieves the index settings for a specified stream and index type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d62a357-e46e-4431-943f-334ae11c8b31">GetIndexWriteSpace</a>
</td>
<td align="left" width="63%">
Retrieves the size of the buffer required to store the completed index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8e9982e-b056-48dc-ac5f-20bf65b475ec">GetSeekPositionForValue</a>
</td>
<td align="left" width="63%">
Given a desired seek time, retrieves the offset from which the client should start reading data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c02931d3-7b43-43a9-9e4e-00945ba3c8d8">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the indexer with the <a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ContentInfo</a> object of the ASF file to be read or encoded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7df6aba2-d63f-4a1a-b6e8-6894f92993b1">SetFlags</a>
</td>
<td align="left" width="63%">
Specifies the read or the write mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f116baaa-8d9b-4ac0-9263-3bb65d67ee63">SetIndexByteStreams</a>
</td>
<td align="left" width="63%">
Sets the byte stream that contains the index entries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bad10893-07af-4b46-bab1-2878553813b5">SetIndexStatus</a>
</td>
<td align="left" width="63%">
Specifies the type of index entries that the indexer must generate for the ASF file.


</td>
</tr>
</table> 


## -remarks



You can use the indexer object to read an existing ASF index or write a new index. The index object has two mutually exclusive modes: read mode and write mode. To set the mode, call <a href="https://msdn.microsoft.com/7df6aba2-d63f-4a1a-b6e8-6894f92993b1">SetFlags</a>. 

Use the following methods to configure the indexer object  (both modes):

<ul>
<li>
<a href="https://msdn.microsoft.com/c02931d3-7b43-43a9-9e4e-00945ba3c8d8">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7df6aba2-d63f-4a1a-b6e8-6894f92993b1">SetFlags</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f116baaa-8d9b-4ac0-9263-3bb65d67ee63">SetIndexByteStreams</a>
</li>
</ul>
Use the following methods to read an existing index:

<ul>
<li>
<a href="https://msdn.microsoft.com/97809620-57ad-48f1-94ba-a2e121cdfee6">GetFlags</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a433af8a-9e8a-4234-9694-c3a5420a1710">GetIndexByteStreamCount</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7ef0e36c-1be5-44ac-8f6a-e29805c99e78">GetIndexPosition</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dc38a060-36e4-458e-829e-2770387fc484">GetIndexStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c8e9982e-b056-48dc-ac5f-20bf65b475ec">GetSeekPositionForValue</a>
</li>
</ul>
Use the following methods to write an index:

<ul>
<li>
<a href="https://msdn.microsoft.com/44b889e1-8860-44fa-b19f-5be9f844a194">CommitIndex</a>
</li>
<li>
<a href="https://msdn.microsoft.com/febc5335-a8e8-4ae9-afb2-17f09b750477">GenerateIndexEntries</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aca721e8-e610-4022-a3da-8ff5a5943e3e">GetCompletedIndex</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8d62a357-e46e-4431-943f-334ae11c8b31">GetIndexWriteSpace</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bad10893-07af-4b46-bab1-2878553813b5">SetIndexStatus</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/df141f8e-10b4-4ac4-8a83-c25764b8f0c6">MFCreateASFIndexer</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

