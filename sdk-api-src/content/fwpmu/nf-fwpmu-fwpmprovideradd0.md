---
UID: NF:fwpmu.FwpmProviderAdd0
title: FwpmProviderAdd0 function
author: windows-driver-content
description: Adds a new provider to the system.
old-location: fwp\fwpmprovideradd0_func.htm
old-project: FWP
ms.assetid: e76f03e2-0853-465a-9f82-c29d35de32c9
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: FwpmProviderAdd0, FwpmProviderAdd0 function [Filtering], fwp.fwpmprovideradd0_func, fwpmu/FwpmProviderAdd0
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
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fwpuclnt.dll
api_name:
-	FwpmProviderAdd0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmProviderAdd0 function


## -description


The <b>FwpmProviderAdd0</b> function   adds a new provider to the system.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param provider [in]

Type: <b>const <a href="https://msdn.microsoft.com/692714fd-14f1-4f8b-a033-1f30b6d0b95a">FWPM_PROVIDER0</a>*</b>

The provider object to be added.


### -param sd [in, optional]

Type: <b><a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">PSECURITY_DESCRIPTOR</a></b>

Security information for the provider object.


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
The provider was successfully added.

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



If the caller supplies a null security descriptor, the system will assign a default security descriptor.

Boot-time objects are added to the Base Filtering Engine (BFE) when the TCP/IP driver starts, and are removed once the BFE finishes initialization.  Persistent objects are added when the BFE starts. If a policy provider has a persistent policy that is not intended to be enforced if its associated service is disabled, the caller can specify an optional service name in the <a href="https://msdn.microsoft.com/692714fd-14f1-4f8b-a033-1f30b6d0b95a">FWPM_PROVIDER0</a> structure.  This service then owns the persistent policy object.  At start, the BFE only adds the following types of persistent objects to the system.

<ul>
<li>The object is not associated with a provider.</li>
<li>The object has an associated provider that does not specify a service name.</li>
<li>The object has an associated provider and an associated service set to auto-start.</li>
</ul>
This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ADD</a> access to the provider's container.  See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmProviderAdd0</b> is a specific implementation of FwpmProviderAdd. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/692714fd-14f1-4f8b-a033-1f30b6d0b95a">FWPM_PROVIDER0</a>
 

 

