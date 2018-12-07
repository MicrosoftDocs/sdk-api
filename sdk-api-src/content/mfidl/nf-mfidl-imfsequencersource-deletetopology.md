---
UID: NF:mfidl.IMFSequencerSource.DeleteTopology
title: IMFSequencerSource::DeleteTopology
author: windows-sdk-content
description: Deletes a topology from the queue.
old-location: mf\imfsequencersource_deletetopology.htm
tech.root: medfound
ms.assetid: 6ef3512d-f953-46a3-8604-bec3904a962f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 6ef3512d-f953-46a3-8604-bec3904a962f, DeleteTopology, DeleteTopology method [Media Foundation], DeleteTopology method [Media Foundation],IMFSequencerSource interface, IMFSequencerSource interface [Media Foundation],DeleteTopology method, IMFSequencerSource.DeleteTopology, IMFSequencerSource::DeleteTopology, mf.imfsequencersource_deletetopology, mfidl/IMFSequencerSource::DeleteTopology
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
 - IMFSequencerSource.DeleteTopology
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSequencerSource::DeleteTopology


## -description



Deletes a topology from the queue.




## -parameters




### -param dwId [in]

The sequencer element identifier of the topology to delete.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ba5e8e7b-5b0e-4807-a459-75bd5727d1e2">IMFSequencerSource</a>



<a href="https://msdn.microsoft.com/788ede68-2fd7-45f6-90cb-2426c40f7d4c">Sequencer Source</a>
 

 

