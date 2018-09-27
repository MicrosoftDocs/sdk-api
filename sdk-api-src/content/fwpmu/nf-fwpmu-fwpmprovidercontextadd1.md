---
UID: NF:fwpmu.FwpmProviderContextAdd1
title: FwpmProviderContextAdd1 function
author: windows-sdk-content
description: Adds a new provider context to the system.
old-location: fwp\fwpmprovidercontextadd1_func.htm
tech.root: FWP
ms.assetid: 2a840f23-96e4-4b3d-b92e-53b3d10ab2bb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FwpmProviderContextAdd1, FwpmProviderContextAdd1 function [Filtering], fwp.fwpmprovidercontextadd1_func, fwpmu/FwpmProviderContextAdd1
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
 - FwpmProviderContextAdd1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmProviderContextAdd1 function


## -description


The <b>FwpmProviderContextAdd1</b> function adds a new provider context to the system.<div class="alert"><b>Note</b>  <b>FwpmProviderContextAdd1</b> is the specific implementation of FwpmProviderContextAdd used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/07c6b1fc-55bb-4526-a24b-0e22f147e5cc">FwpmProviderContextAdd2</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/c31595b8-81e4-4399-b2a3-d228c35875fe">FwpmProviderContextAdd0</a> is available.</div>
<div> </div>



## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param providerContext [in]

Type: <b>const <a href="https://msdn.microsoft.com/34727579-9baf-4d50-b973-e864ddf651b0">FWPM_PROVIDER_CONTEXT1</a>*</b>

The provider context object to be added.


### -param sd [in, optional]

Type: <b><a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">PSECURITY_DESCRIPTOR</a></b>

Security information associated with the provider context object.


### -param id [out, optional]

Type: <b>UINT64*</b>

Pointer to a variable that receives a runtime identifier for this provider context.


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
The provider context was successfully added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
<dt>0x32</dt>
</dl>
</td>
<td width="60%">
The <b>type</b> member of the <i>providerContext</i> parameter is  <a href="https://msdn.microsoft.com/e8eae5e7-9240-47a5-851b-1ec51cb07b63">FWPM_IPSEC_IKE_MM_CONTEXT</a>and     the <b>ikeMmPolicy</b> member of the <i>providerContext</i> parameter contains an <a href="https://msdn.microsoft.com/582ec1ea-9390-4f86-9a3c-25d4e805a218">IKEEXT_IPV6_CGA</a> authentication method in the <b>authenticationMethods</b> array, but cryptographically generated address (CGA) is not enabled in
      the registry.

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



Some fields in the <a href="https://msdn.microsoft.com/34727579-9baf-4d50-b973-e864ddf651b0">FWPM_PROVIDER_CONTEXT1</a> structure are assigned by the system, not the caller, and are ignored in the call to <b>FwpmProviderContextAdd1</b>. 

If the caller supplies a <b>NULL</b> security descriptor, the system will assign a default security descriptor.

This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ADD</a> access to the provider context's container and <b>FWPM_ACTRL_ADD_LINK</b> access to the provider (if any).  See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/34727579-9baf-4d50-b973-e864ddf651b0">FWPM_PROVIDER_CONTEXT1</a>
 

 

