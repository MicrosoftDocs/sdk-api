---
UID: NF:wmcontainer.IMFASFIndexer.GenerateIndexEntries
title: IMFASFIndexer::GenerateIndexEntries
author: windows-sdk-content
description: Accepts an ASF packet for the file and creates index entries for them.
old-location: mf\imfasfindexer_generateindexentries.htm
old-project: medfound
ms.assetid: febc5335-a8e8-4ae9-afb2-17f09b750477
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GenerateIndexEntries, GenerateIndexEntries method [Media Foundation], GenerateIndexEntries method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GenerateIndexEntries method, IMFASFIndexer.GenerateIndexEntries, IMFASFIndexer::GenerateIndexEntries, febc5335-a8e8-4ae9-afb2-17f09b750477, mf.imfasfindexer_generateindexentries, wmcontainer/IMFASFIndexer::GenerateIndexEntries
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFIndexer.GenerateIndexEntries
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFIndexer::GenerateIndexEntries


## -description


Accepts an ASF packet for the file and creates index entries for them.


## -parameters




### -param pIASFPacketSample [in]

Pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of a media sample that contains the ASF packet.
          


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument passed in is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The indexer is not initialized.

</td>
</tr>
</table>
 




## -remarks



The ASF indexer creates indexes for a file internally. You can get the completed index for all data packets sent to the indexer by committing the index with <a href="https://msdn.microsoft.com/44b889e1-8860-44fa-b19f-5be9f844a194">IMFASFIndexer::CommitIndex</a> and then calling <a href="https://msdn.microsoft.com/aca721e8-e610-4022-a3da-8ff5a5943e3e">IMFASFIndexer::GetCompletedIndex</a> to write the index entries into a media buffer. To determine the size of the index so you can allocate a buffer large enough to hold the index, call <a href="https://msdn.microsoft.com/8d62a357-e46e-4431-943f-334ae11c8b31">IMFASFIndexer::GetIndexWriteSpace</a>.

When this method creates index entries, they are immediately available for use by <a href="https://msdn.microsoft.com/c8e9982e-b056-48dc-ac5f-20bf65b475ec">IMFASFIndexer::GetSeekPositionForValue</a>.
      

The media sample specified in   <i>pIASFPacketSample</i> must hold a buffer that contains a single ASF packet. Get the sample from the  ASF multiplexer by calling the <a href="https://msdn.microsoft.com/39b9f8a0-fb26-4f46-98fd-b4636f8f88c7">IMFASFMultiplexer::GetNextPacket</a> method. 

You cannot use this method while reading an index, only when writing an index.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 

