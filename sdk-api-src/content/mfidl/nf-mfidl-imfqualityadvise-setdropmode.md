---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFQualityAdvise::SetDropMode


## -description



Sets the drop mode. In drop mode, a component drops samples, more or less aggressively depending on the level of the drop mode.




## -parameters




### -param eDropMode [in]

Requested drop mode, specified as a member of the <a href="https://msdn.microsoft.com/e40751d2-9abf-4fe6-8829-9b1fbf4531e8">MF_QUALITY_DROP_MODE</a> enumeration.


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
<dt><b>MF_E_NO_MORE_DROP_MODES</b></dt>
</dl>
</td>
<td width="60%">
The component does not support the specified mode or any higher modes.

</td>
</tr>
</table>
 




## -remarks



If this method is called on a media source, the media source might switch between thinned and non-thinned output. If that occurs, the affected streams will send an <a href="https://msdn.microsoft.com/7de8cb64-122a-475f-990c-c19590a9d9d8">MEStreamThinMode</a> event to indicate the transition. The operation is asynchronous; after <b>SetDropMode</b> returns, you might receive samples that were queued before the transition. The MEStreamThinMode event marks the exact point in the stream where the transition occurs.




## -see-also




<a href="https://msdn.microsoft.com/20681ce7-e07e-4e34-9238-ec23cc6bfc84">IMFQualityAdvise</a>
 

 

