---
UID: NF:fwpmu.FwpmCalloutAdd0
title: FwpmCalloutAdd0 function
author: windows-sdk-content
description: Adds a new callout object to the system.
old-location: fwp\fwpmcalloutadd0_func.htm
tech.root: FWP
ms.assetid: e4f79262-6345-49e9-a50c-9f8a82f2df0e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FwpmCalloutAdd0, FwpmCalloutAdd0 function [Filtering], fwp.fwpmcalloutadd0_func, fwpmu/FwpmCalloutAdd0
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
 - FwpmCalloutAdd0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmCalloutAdd0 function


## -description


The <b>FwpmCalloutAdd0</b> function adds a new callout object to the system.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param callout [in]

Type: <b>const <a href="https://msdn.microsoft.com/4f565de5-5bc9-4508-9e4b-28d14a82a9a5">FWPM_CALLOUT0</a>*</b>

The callout object to be added.


### -param sd [in, optional]

Type: <b><a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">PSECURITY_DESCRIPTOR</a></b>

The security information associated with the callout.


### -param id [out, optional]

Type: <b>UINT32*</b>

Runtime identifier for this callout.


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
The callout was successfully added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_INVALID_PARAMETER</b></dt>
<dt>0x80320035</dt>
</dl>
</td>
<td width="60%">
FWPM_TUNNEL_FLAG_POINT_TO_POINT was not set and conditions other than local/remote
   address were specified.

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



Some fields in the <a href="https://msdn.microsoft.com/4f565de5-5bc9-4508-9e4b-28d14a82a9a5">FWPM_CALLOUT0</a> structure are assigned by the system, not the caller, and are ignored in the call to <b>FwpmCalloutAdd0</b>. If the caller supplies a null security descriptor, the system will assign a default security descriptor.

This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ADD</a> access to the callout's container, 
   <b>FWPM_ACTRL_ADD_LINK </b> access to the provider (if any), and 
   <b>FWPM_ACTRL_ADD_LINK </b> access to the applicable layer. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

To add a filter that references a callout, invoke the functions in the following order.

<ul>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=199850">FwpsCalloutRegister</a> (documented in the Windows Driver Kit (WDK)), to register the callout with the filter engine.</li>
<li>Call <b>FwpmCalloutAdd0</b> to add the callout to the system.</li>
<li>Call <a href="https://msdn.microsoft.com/ca11187e-3a91-438f-9a7f-606da7c88f6d">FwpmFilterAdd0</a> to add the filter that references the callout to the system.</li>
</ul>
  
By default filters that reference callouts that have been added but have not yet registered with the filter engine are treated as Block filters.

<b>FwpmCalloutAdd0</b> is a specific implementation of FwpmCalloutAdd. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/4f565de5-5bc9-4508-9e4b-28d14a82a9a5">FWPM_CALLOUT0</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=98328">Kernel-Mode FwpmCalloutAdd0</a>
 

 

