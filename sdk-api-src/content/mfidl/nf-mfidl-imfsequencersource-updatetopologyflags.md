---
UID: NF:mfidl.IMFSequencerSource.UpdateTopologyFlags
title: IMFSequencerSource::UpdateTopologyFlags method
author: windows-driver-content
description: Updates the flags for a topology in the queue.
old-location: mf\imfsequencersource_updatetopologyflags.htm
old-project: medfound
ms.assetid: ee71b574-0456-4091-bbb0-da5c57a7506e
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFSequencerSource, IMFSequencerSource interface [Media Foundation], UpdateTopologyFlags method, IMFSequencerSource::UpdateTopologyFlags, UpdateTopologyFlags method [Media Foundation], UpdateTopologyFlags method [Media Foundation], IMFSequencerSource interface, UpdateTopologyFlags,IMFSequencerSource.UpdateTopologyFlags, ee71b574-0456-4091-bbb0-da5c57a7506e, mf.imfsequencersource_updatetopologyflags, mfidl/IMFSequencerSource::UpdateTopologyFlags
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFSequencerSource.UpdateTopologyFlags
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSequencerSource::UpdateTopologyFlags method


## -description



Updates the flags for a topology in the queue.




## -parameters




### -param dwId [in]

Sequencer element identifier of the topology to update.


### -param dwFlags [in]

Bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/d52bac8c-e490-417c-ac00-e4cf57fd151c">MFSequencerTopologyFlags</a> enumeration.


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
 

 

