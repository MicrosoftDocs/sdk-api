---
UID: NF:fwpmu.FwpmNetEventSubscriptionsGet0
title: FwpmNetEventSubscriptionsGet0 function
author: windows-driver-content
description: Retrieves an array of all the current net event notification subscriptions.
old-location: fwp\fwpmneteventsubscriptionsget0.htm
old-project: FWP
ms.assetid: 08a5378d-b9f7-45d9-b63c-fabcd94b717c
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: FwpmNetEventSubscriptionsGet0, FwpmNetEventSubscriptionsGet0 function [Filtering], fwp.fwpmneteventsubscriptionsget0, fwpmu/FwpmNetEventSubscriptionsGet0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fwpmu.h
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
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fwpuclnt.dll
api_name:
-	FwpmNetEventSubscriptionsGet0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmNetEventSubscriptionsGet0 function


## -description


The <b>FwpmNetEventSubscriptionsGet0</b> function retrieves an array of all the current net event notification subscriptions.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param entries [out]

Type: <b><a href="https://msdn.microsoft.com/a1aa8369-fd70-46f6-983d-0afdf8b8ff77">FWPM_NET_EVENT_SUBSCRIPTION0</a>***</b>

The current net event notification subscriptions.


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

<b>FwpmNetEventSubscriptionsGet0</b> is a specific implementation of FwpmNetEventSubscriptionsGet. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/a1aa8369-fd70-46f6-983d-0afdf8b8ff77">FWPM_NET_EVENT_SUBSCRIPTION0</a>
 

 

