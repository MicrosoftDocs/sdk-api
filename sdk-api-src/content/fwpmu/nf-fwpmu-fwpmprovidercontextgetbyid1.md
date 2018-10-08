---
UID: NF:fwpmu.FwpmProviderContextGetById1
title: FwpmProviderContextGetById1 function
author: windows-sdk-content
description: Retrieves a provider context.
old-location: fwp\fwpmprovidercontextgetbyid1_func.htm
tech.root: fwp
ms.assetid: 76353efa-844e-4c7f-9f9a-0bf2e247c58b
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: FwpmProviderContextGetById1, FwpmProviderContextGetById1 function [Filtering], fwp.fwpmprovidercontextgetbyid1_func, fwpmu/FwpmProviderContextGetById1
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
 - FwpmProviderContextGetById1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmProviderContextGetById1 function


## -description


The <b>FwpmProviderContextGetById1</b> function retrieves a provider context.
<div class="alert"><b>Note</b>  <b>FwpmProviderContextGetById1</b> is the specific implementation of FwpmProviderContextGetById used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/50578a7a-d869-4fad-a159-f69a234069e6">FwpmProviderContextGetById2</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/afa32d9b-17fd-44f0-b2df-119ca3aed5cd">FwpmProviderContextGetById0</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param id [in]

Type: <b>UINT64</b>

A run-time identifier for the desired object. This must be the run-time identifier that was received from the system when the application called <a href="https://msdn.microsoft.com/2a840f23-96e4-4b3d-b92e-53b3d10ab2bb">FwpmProviderContextAdd1</a> for this object.


### -param providerContext [out]

Type: <b><a href="https://msdn.microsoft.com/34727579-9baf-4d50-b973-e864ddf651b0">FWPM_PROVIDER_CONTEXT1</a>**</b>

The provider context information.


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
The provider context was retrieved successfully.

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

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ</a> access to the provider context. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/34727579-9baf-4d50-b973-e864ddf651b0">FWPM_PROVIDER_CONTEXT1</a>



<a href="https://msdn.microsoft.com/2a840f23-96e4-4b3d-b92e-53b3d10ab2bb">FwpmProviderContextAdd1</a>
 

 

