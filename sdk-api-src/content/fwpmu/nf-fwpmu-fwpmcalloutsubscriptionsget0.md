---
UID: NF:fwpmu.FwpmCalloutSubscriptionsGet0
title: FwpmCalloutSubscriptionsGet0 function
author: windows-sdk-content
description: Retrieves an array of all the current callout change notification subscriptions.
old-location: fwp\fwpmcalloutsubscriptionsget0_func.htm
tech.root: FWP
ms.assetid: 72e51167-c69e-4412-b83e-c66f91c9b96e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FwpmCalloutSubscriptionsGet0, FwpmCalloutSubscriptionsGet0 function [Filtering], fwp.fwpmcalloutsubscriptionsget0_func, fwpmu/FwpmCalloutSubscriptionsGet0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fwpmu.h
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmCalloutSubscriptionsGet0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmCalloutSubscriptionsGet0 function


## -description


The <b>FwpmCalloutSubscriptionsGet0</b> function retrieves an array of all the current callout change notification subscriptions.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param entries [out]

Type: <b><a href="https://msdn.microsoft.com/35afdc09-0745-4d59-9be1-d360b02fbd2f">FWPM_CALLOUT_SUBSCRIPTION0</a>***</b>

Addresses of the current callout change notification subscriptions.


### -param numEntries [out]

Type: <b>UINT32*</b>

The number of entries returned.


## -returns



Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The subscriptions were retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="https://msdn.microsoft.com/11f3085a-f044-4a78-b47a-59b9086562bf">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>
 




## -remarks



The returned array (but not the individual entries in the array) must be freed through a call to <a href="https://msdn.microsoft.com/ba9f8c1e-f75c-4bf0-b68b-e21a358575fc">FwpmFreeMemory0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ</a> access to the callout's container. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmCalloutSubscriptionsGet0</b> is a specific implementation of FwpmCalloutSubscriptionsGet. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/35afdc09-0745-4d59-9be1-d360b02fbd2f">FWPM_CALLOUT_SUBSCRIPTION0</a>
 

 

