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

# IMFMediaEngineOPMInfo::GetOPMInfo


## -description


Gets status information about the   <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>  (OPM).


## -parameters




### -param pStatus [out]

        A pointer to a <a href="https://msdn.microsoft.com/7C4D88F6-369B-4364-90C4-6D0F8DD1523B">MF_MEDIA_ENGINE_OPM_STATUS</a> enum type that indicates the OPM status.


### -param pConstricted [out]

A pointer to a <b>BOOL</b> type that indicates the constriction status.


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
The method succeeded

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
If any of the parameters are <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/399f81ac-38f8-4aaa-8b34-f5fd13b71402">IMFMediaEngineOPMInfo</a>
 

 

