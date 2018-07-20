---
UID: NF:wmcontainer.IMFASFIndexer.SetIndexByteStreams
title: IMFASFIndexer::SetIndexByteStreams
author: windows-sdk-content
description: Adds byte streams to be indexed.
old-location: mf\imfasfindexer_setindexbytestreams.htm
old-project: medfound
ms.assetid: f116baaa-8d9b-4ac0-9263-3bb65d67ee63
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFASFIndexer interface [Media Foundation],SetIndexByteStreams method, IMFASFIndexer.SetIndexByteStreams, IMFASFIndexer::SetIndexByteStreams, SetIndexByteStreams, SetIndexByteStreams method [Media Foundation], SetIndexByteStreams method [Media Foundation],IMFASFIndexer interface, f116baaa-8d9b-4ac0-9263-3bb65d67ee63, mf.imfasfindexer_setindexbytestreams, wmcontainer/IMFASFIndexer::SetIndexByteStreams
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
 - IMFASFIndexer.SetIndexByteStreams
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFIndexer::SetIndexByteStreams


## -description



Adds byte streams to be indexed.




## -parameters




### -param ppIByteStreams [in]

An array of <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface pointers. To get the byte stream, call <a href="https://msdn.microsoft.com/edcce9d4-9296-4b39-8e58-58ae602c250f">MFCreateASFIndexerByteStream</a>.


### -param cByteStreams [in]

The number of pointers in the <i>ppIByteStreams</i> array.


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
<dt><b>MF_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The indexer object has already been initialized and it  has packets which have been indexed.

</td>
</tr>
</table>
 




## -remarks



For a reading scenario, only one byte stream should be used by the indexer object. For an index generating scenario, it depends how many index objects are needed to be generated. 




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 

