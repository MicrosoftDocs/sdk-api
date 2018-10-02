---
UID: NF:ndfapi.NdfRepairIncident
title: NdfRepairIncident function
author: windows-sdk-content
description: Repairs an incident without displaying a user interface.
old-location: ndf\ndfrepairincident.htm
tech.root: NDF
ms.assetid: 570e7824-463f-4fc1-bc1a-16a1da31e8a3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NdfRepairIncident, NdfRepairIncident function [NDF], ndf.ndfrepairincident, ndfapi/NdfRepairIncident
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ndfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - NdfRepairIncident
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdfRepairIncident function


## -description


The <b>NdfRepairIncident</b> function repairs an incident without displaying a user interface.


## -parameters




### -param Handle [in]

Type: <b>NDFHANDLE</b>

Handle to the Network Diagnostics Framework incident. This handle should match the handle passed to <a href="https://msdn.microsoft.com/69ae5624-7c3b-44a2-8468-d587739fc666">NdfDiagnoseIncident</a>.


### -param RepairEx [in]

Type: <b><a href="https://msdn.microsoft.com/9357f463-946c-47ad-bb8d-ff9de210e7e1">RepairInfoEx</a>*</b>

A structure (obtained from <a href="https://msdn.microsoft.com/69ae5624-7c3b-44a2-8468-d587739fc666">NdfDiagnoseIncident</a>) which indicates the particular repair to be performed.

Memory allocated to these structures should later be freed.  For an example of how to do this, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=158047">Microsoft Windows Network Diagnostics Samples</a>.


### -param dwWait

Type: <b>DWORD</b>

The length of time, in milliseconds, to wait before terminating the diagnostic routine. INFINITE may be passed to this parameter if no timeout is desired.


## -returns



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
Repair succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDF_E_VALIDATION</b></dt>
</dl>
</td>
<td width="60%">
The repair executed successfully, but NDF validation still found a connectivity problem. If this value is returned, the session should be closed by calling <a href="https://msdn.microsoft.com/5e5caf41-ca24-42e0-ac22-3b569400c383">NdfCloseIncident</a> and another session should be created to continue the diagnosis.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The NDF incident handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The repair operation has terminated because it has taken longer than the time-out specified in dwWait.

</td>
</tr>
</table>
 

Other failure codes are returned if the repair failed to execute. In that case, the client can call <b>NdfRepairIncident</b> again with a different repair. 




## -remarks



<b>NdfRepairIncident</b> can only be called when <a href="https://msdn.microsoft.com/69ae5624-7c3b-44a2-8468-d587739fc666">NdfDiagnoseIncident</a> is used for diagnostics. This is typically the case in scenarios where no user interface is shown, or where the standard Windows experience is not being used (as with Media Center and embedded applications). <b>NdfRepairIncident</b> should not be called when <a href="https://msdn.microsoft.com/b65f30c3-53d5-4282-8d38-5723772f15fc">NdfExecuteDiagnosis</a> is used.

Before using this API, an application must call an incident creation function such as <a href="https://msdn.microsoft.com/28ca2949-6867-4c9a-aebc-bf2a57627c04">NdfCreateWebIncident</a> to begin the NDF diagnostics process. The application then calls <a href="https://msdn.microsoft.com/69ae5624-7c3b-44a2-8468-d587739fc666">NdfDiagnoseIncident</a> to diagnose the issue. If the diagnostics process identifies some possible repairs, the application can call <b>NdfRepairIncident</b> to repair the problem without displaying a user interface. <a href="https://msdn.microsoft.com/dc0cbfc0-fcaa-44b2-a753-8df9f184b8ca">NdfCancelIncident</a> can optionally be called from a separate thread if the application wants to cancel an ongoing <b>NdfRepairIncident</b> call. Finally, the application calls <a href="https://msdn.microsoft.com/5e5caf41-ca24-42e0-ac22-3b569400c383">NdfCloseIncident</a>.




## -see-also




<a href="https://msdn.microsoft.com/69ae5624-7c3b-44a2-8468-d587739fc666">NdfDiagnoseIncident</a>



<a href="https://msdn.microsoft.com/9357f463-946c-47ad-bb8d-ff9de210e7e1">RepairInfoEx</a>
 

 

