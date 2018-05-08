---
UID: NF:wmcontainer.IMFASFIndexer.GetIndexStatus
title: IMFASFIndexer::GetIndexStatus
author: windows-driver-content
description: Retrieves the index settings for a specified stream and index type.
old-location: mf\imfasfindexer_getindexstatus.htm
old-project: medfound
ms.assetid: dc38a060-36e4-458e-829e-2770387fc484
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetIndexStatus, GetIndexStatus method [Media Foundation], GetIndexStatus method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetIndexStatus method, IMFASFIndexer.GetIndexStatus, IMFASFIndexer::GetIndexStatus, dc38a060-36e4-458e-829e-2770387fc484, mf.imfasfindexer_getindexstatus, wmcontainer/IMFASFIndexer::GetIndexStatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFASFIndexer.GetIndexStatus
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFIndexer::GetIndexStatus


## -description



Retrieves the index settings for a specified stream and index type.




## -parameters




### -param pIndexIdentifier [in]

Pointer to an <a href="https://msdn.microsoft.com/8103a62e-6d1a-4dcd-af91-cedb30523004">ASF_INDEX_IDENTIFIER</a> structure that contains the stream number and index type for which to get the status.


### -param pfIsIndexed [out]

A variable that retrieves a Boolean value specifying whether the index described by <i>pIndexIdentifier</i> has been created.


### -param pbIndexDescriptor [out]

A buffer that receives the index descriptor. The index descriptor consists of an <a href="https://msdn.microsoft.com/2a540aef-068d-4465-b0ed-64aed828af01">ASF_INDEX_DESCRIPTOR</a> structure, optionally followed by index-specific data.


### -param pcbIndexDescriptor [in, out]

On input, specifies the size, in bytes, of the buffer that <i>pbIndexDescriptor</i> points to. The value can be zero if <i>pbIndexDescriptor</i> is <b>NULL</b>. On output, receives the size of the index descriptor, in bytes.


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
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer size specified in <i>pcbIndexDescriptor</i> is too small.

</td>
</tr>
</table>
 




## -remarks



To read an existing ASF index, call <a href="https://msdn.microsoft.com/f116baaa-8d9b-4ac0-9263-3bb65d67ee63">IMFASFIndexer::SetIndexByteStreams</a> before calling this method.

If an index exists for the stream and the value passed into <i>pcbIndexDescriptor</i> is smaller than the required size of the <i>pbIndexDescriptor</i> buffer, the method returns MF_E_BUFFERTOOSMALL. The required buffer size is returned in the <i>pcbIndexDescriptor</i> parameter.

If there is no index for the specified stream, the method returns <b>FALSE</b> in the <i>pfIsIndexed</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 

