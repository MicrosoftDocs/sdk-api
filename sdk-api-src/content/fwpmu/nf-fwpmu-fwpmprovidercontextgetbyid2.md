---
UID: NF:fwpmu.FwpmProviderContextGetById2
title: FwpmProviderContextGetById2 function
author: windows-sdk-content
description: Retrieves a provider context.
old-location: fwp\fwpmprovidercontextgetbyid2.htm
old-project: FWP
ms.assetid: 50578a7a-d869-4fad-a159-f69a234069e6
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FwpmProviderContextGetById2, FwpmProviderContextGetById2 function [Filtering], fwp.fwpmprovidercontextgetbyid2, fwpmu/FwpmProviderContextGetById2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
-	fwpuclnt.dll
api_name:
-	FwpmProviderContextGetById2
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmProviderContextGetById2 function


## -description


The <b>FwpmProviderContextGetById2</b> function retrieves a provider context.
<div class="alert"><b>Note</b>  <b>FwpmProviderContextGetById2</b> is the specific implementation of FwpmProviderContextGetById used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/76353efa-844e-4c7f-9f9a-0bf2e247c58b">FwpmProviderContextGetById1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/afa32d9b-17fd-44f0-b2df-119ca3aed5cd">FwpmProviderContextGetById0</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param id [in]

Type: <b>UINT64</b>

A run-time identifier for the desired object. This must be the run-time identifier that was received from the system when the application called <a href="https://msdn.microsoft.com/07c6b1fc-55bb-4526-a24b-0e22f147e5cc">FwpmProviderContextAdd2</a> for this object.


### -param providerContext [out]

Type: <b><a href="https://msdn.microsoft.com/aa397a4e-07cc-4eee-8d0f-798901a5bb29">FWPM_PROVIDER_CONTEXT2</a>**</b>

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




<a href="https://msdn.microsoft.com/aa397a4e-07cc-4eee-8d0f-798901a5bb29">FWPM_PROVIDER_CONTEXT2</a>



<a href="https://msdn.microsoft.com/07c6b1fc-55bb-4526-a24b-0e22f147e5cc">FwpmProviderContextAdd2</a>
 

 

