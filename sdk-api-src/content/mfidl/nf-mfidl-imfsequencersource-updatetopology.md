---
UID: NF:mfidl.IMFSequencerSource.UpdateTopology
title: IMFSequencerSource::UpdateTopology
author: windows-sdk-content
description: Updates a topology in the queue.
old-location: mf\imfsequencersource_updatetopology.htm
old-project: medfound
ms.assetid: 4ed6be6c-a031-4628-a3c5-7f0676cc0baf
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 4ed6be6c-a031-4628-a3c5-7f0676cc0baf, IMFSequencerSource interface [Media Foundation],UpdateTopology method, IMFSequencerSource.UpdateTopology, IMFSequencerSource::UpdateTopology, UpdateTopology, UpdateTopology method [Media Foundation], UpdateTopology method [Media Foundation],IMFSequencerSource interface, mf.imfsequencersource_updatetopology, mfidl/IMFSequencerSource::UpdateTopology
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFSequencerSource.UpdateTopology
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSequencerSource::UpdateTopology


## -description



Updates a topology in the queue.




## -parameters




### -param dwId [in]

Sequencer element identifier of the topology to update.


### -param pTopology [in]

Pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the updated topology object.


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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The sequencer source has been shut down.

</td>
</tr>
</table>
 




## -remarks



This method is asynchronous. When the operation is completed, the sequencer source sends an <a href="https://msdn.microsoft.com/f573cbd0-689c-4bfe-846b-6fc8008101c8">MESequencerSourceTopologyUpdated</a> event.




## -see-also




<a href="https://msdn.microsoft.com/ba5e8e7b-5b0e-4807-a459-75bd5727d1e2">IMFSequencerSource</a>



<a href="https://msdn.microsoft.com/788ede68-2fd7-45f6-90cb-2426c40f7d4c">Sequencer Source</a>
 

 

