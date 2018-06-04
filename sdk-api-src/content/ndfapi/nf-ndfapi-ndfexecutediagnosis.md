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

# NdfExecuteDiagnosis function


## -description


The <b>NdfExecuteDiagnosis</b> function is used to diagnose the root cause of the incident that has occurred.


## -parameters




### -param handle

Type: <b>NDFHANDLE</b>

Handle to the Network Diagnostics Framework incident.


### -param hwnd

Type: <b>HWND</b>

Handle to the window that is intended to display the diagnostic information. If specified, the NDF UI is modal to the window.  If <b>NULL</b>, the UI is non-modal.


## -returns



Type: <b>HRESULT</b>

Possible return values include, but are not limited to, the following.

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
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>handle</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e5caf41-ca24-42e0-ac22-3b569400c383">NdfCloseIncident</a>



<a href="https://msdn.microsoft.com/8570a0e2-f02f-4812-a5c8-13b6e5feee6f">NdfCreateIncident</a>



<a href="https://msdn.microsoft.com/c4cb2713-b656-47a8-9de7-9d33e864a811">NdfCreateWinSockIncident</a>
 

 

