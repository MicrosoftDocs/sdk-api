---
UID: NF:ndfapi.NdfExecuteDiagnosis
title: NdfExecuteDiagnosis function (ndfapi.h)
author: windows-sdk-content
description: The NdfExecuteDiagnosis function is used to diagnose the root cause of the incident that has occurred.
old-location: ndf\ndfexecutediagnosis.htm
tech.root: NDF
ms.assetid: b65f30c3-53d5-4282-8d38-5723772f15fc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NdfExecuteDiagnosis, NdfExecuteDiagnosis function [NDF], ndf.ndfexecutediagnosis, ndfapi/NdfExecuteDiagnosis
ms.topic: function
req.header: ndfapi.h
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
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ndfapi.dll
api_name:
 - NdfExecuteDiagnosis
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
 

 

