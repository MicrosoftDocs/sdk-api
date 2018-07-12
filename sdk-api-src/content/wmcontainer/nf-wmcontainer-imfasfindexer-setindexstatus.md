---
UID: NF:wmcontainer.IMFASFIndexer.SetIndexStatus
title: IMFASFIndexer::SetIndexStatus
author: windows-sdk-content
description: Configures the index for a stream.
old-location: mf\imfasfindexer_setindexstatus.htm
old-project: medfound
ms.assetid: bad10893-07af-4b46-bab1-2878553813b5
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFASFIndexer interface [Media Foundation],SetIndexStatus method, IMFASFIndexer.SetIndexStatus, IMFASFIndexer::SetIndexStatus, SetIndexStatus, SetIndexStatus method [Media Foundation], SetIndexStatus method [Media Foundation],IMFASFIndexer interface, bad10893-07af-4b46-bab1-2878553813b5, mf.imfasfindexer_setindexstatus, wmcontainer/IMFASFIndexer::SetIndexStatus
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
 - IMFASFIndexer.SetIndexStatus
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFIndexer::SetIndexStatus


## -description



Configures the index for a stream.




## -parameters




### -param pbIndexDescriptor




### -param cbIndexDescriptor [in]

The size, in bytes, of the index descriptor.


### -param fGenerateIndex [in]

A Boolean value. Set to <b>TRUE</b> to have the indexer create an index of the type specified for the stream specified in the index descriptor.


#### - pIndexDescriptor [in]

The index descriptor to set. The index descriptor is an <a href="https://msdn.microsoft.com/2a540aef-068d-4465-b0ed-64aed828af01">ASF_INDEX_DESCRIPTOR</a> structure, optionally followed by index-specific data.


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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
At attempt was made to change the index status in a seek-only scenario. For more information, see Remarks.

</td>
</tr>
</table>
 




## -remarks



You must make all calls to <b>SetIndexStatus</b> before making any calls to <a href="https://msdn.microsoft.com/febc5335-a8e8-4ae9-afb2-17f09b750477">IMFASFIndexer::GenerateIndexEntries</a>.

The indexer object is configured to create temporal indexes for each stream by default. Call this method only if you want to override the default settings.

You cannot use this method in an index reading scenario.  You can only use this method when writing indexes.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 

