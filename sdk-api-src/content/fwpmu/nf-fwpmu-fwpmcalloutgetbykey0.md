---
UID: NF:fwpmu.FwpmCalloutGetByKey0
title: FwpmCalloutGetByKey0 function
author: windows-sdk-content
description: Retrieves a callout object.
old-location: fwp\fwpmcalloutgetbykey0_func.htm
tech.root: fwp
ms.assetid: 05c5ac43-adf1-419c-8a39-32f8dddd3b98
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FwpmCalloutGetByKey0, FwpmCalloutGetByKey0 function [Filtering], fwp.fwpmcalloutgetbykey0_func, fwpmu/FwpmCalloutGetByKey0
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
 - FwpmCalloutGetByKey0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmCalloutGetByKey0 function


## -description


The <b>FwpmCalloutGetByKey0</b> function retrieves a callout object.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param key [in]

Type: <b>const GUID*</b>

Unique identifier of the callout. This GUID was specified in the <b>calloutKey</b> member of the <i>callout</i> parameter when the application called <a href="https://msdn.microsoft.com/e4f79262-6345-49e9-a50c-9f8a82f2df0e">FwpmCalloutAdd0</a> for this object.


### -param callout [out]

Type: <b><a href="https://msdn.microsoft.com/4f565de5-5bc9-4508-9e4b-28d14a82a9a5">FWPM_CALLOUT0</a>**</b>

Information about the state associated with the callout.


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
The callout was retrieved successfully.

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



The caller must free the returned object by a call to <a href="https://msdn.microsoft.com/ba9f8c1e-f75c-4bf0-b68b-e21a358575fc">FwpmFreeMemory0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ</a> access to the callout. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmCalloutGetByKey0</b> is a specific implementation of FwpmCalloutGetByKey. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/4f565de5-5bc9-4508-9e4b-28d14a82a9a5">FWPM_CALLOUT0</a>



<a href="https://msdn.microsoft.com/e4f79262-6345-49e9-a50c-9f8a82f2df0e">FwpmCalloutAdd0</a>
 

 

