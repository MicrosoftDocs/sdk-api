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

# NdfCancelIncident function


## -description


The <b>NdfCancelIncident</b> function is used to cancel unneeded functions which have been previously called on an existing incident.


## -parameters




### -param Handle [in]

Type: <b>NDFHANDLE</b>

Handle to the Network Diagnostics Framework incident. This handle should match the handle of an existing incident.


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
</table>
 

 Any result other than S_OK should be interpreted as an error.




## -remarks



Before using this API, an application must call an incident creation function such as <a href="https://msdn.microsoft.com/28ca2949-6867-4c9a-aebc-bf2a57627c04">NdfCreateWebIncident</a>.

<b>NdfCancelIncident</b> is primarily used to cancel calls to functions such as <a href="https://msdn.microsoft.com/69ae5624-7c3b-44a2-8468-d587739fc666">NdfDiagnoseIncident</a> or <a href="https://msdn.microsoft.com/570e7824-463f-4fc1-bc1a-16a1da31e8a3">NdfRepairIncident</a> which have been previously called, but are no longer needed. When <b>NdfCancelIncident</b> is called, NDF will stop the diagnosis/repair as soon as possible rather than calling the other functions (unless results have already been returned from those functions, in which case <b>NdfCancelIncident</b> will have no effect).


<a href="https://msdn.microsoft.com/5e5caf41-ca24-42e0-ac22-3b569400c383">NdfCloseIncident</a> should be used to close an incident once it has been resolved, as <b>NdfCancelIncident</b> does not actually close the incident itself.



