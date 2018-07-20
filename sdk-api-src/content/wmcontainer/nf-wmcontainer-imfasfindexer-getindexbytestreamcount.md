---
UID: NF:wmcontainer.IMFASFIndexer.GetIndexByteStreamCount
title: IMFASFIndexer::GetIndexByteStreamCount
author: windows-sdk-content
description: Retrieves the number of byte streams that are in use by the indexer object.
old-location: mf\imfasfindexer_getindexbytestreamcount.htm
old-project: medfound
ms.assetid: a433af8a-9e8a-4234-9694-c3a5420a1710
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetIndexByteStreamCount, GetIndexByteStreamCount method [Media Foundation], GetIndexByteStreamCount method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetIndexByteStreamCount method, IMFASFIndexer.GetIndexByteStreamCount, IMFASFIndexer::GetIndexByteStreamCount, a433af8a-9e8a-4234-9694-c3a5420a1710, mf.imfasfindexer_getindexbytestreamcount, wmcontainer/IMFASFIndexer::GetIndexByteStreamCount
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
 - IMFASFIndexer.GetIndexByteStreamCount
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFIndexer::GetIndexByteStreamCount


## -description



Retrieves the number of byte streams that are  in use by the  indexer object.




## -parameters




### -param pcByteStreams [out]

Receives the number of byte streams that are  in use by the indexer object.


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
<i>pcByteStreams</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 

