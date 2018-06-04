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

# IForegroundTransfer::AllowForegroundTransfer


## -description


Yields the foreground window to the COM server process.


## -parameters




### -param lpvReserved [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvReserved</i> parameter is not <b>NULL</b>, or this interface is on a proxy that does not support foreground control.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a728aaad-3d7a-425c-b886-ba35c4fa54d0">CoAllowSetForegroundWindow</a>



<a href="https://msdn.microsoft.com/21857592-0f98-4eb4-a153-4ce20edf26c7">IForegroundTransfer</a>
 

 

