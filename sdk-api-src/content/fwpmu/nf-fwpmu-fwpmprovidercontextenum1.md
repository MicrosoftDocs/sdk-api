---
UID: NF:fwpmu.FwpmProviderContextEnum1
title: FwpmProviderContextEnum1 function
author: windows-sdk-content
description: Returns the next page of results from the provider context enumerator.
old-location: fwp\fwpmprovidercontextenum1_func.htm
tech.root: fwp
ms.assetid: 97a6e562-0423-438d-ab21-48c0f0830610
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FwpmProviderContextEnum1, FwpmProviderContextEnum1 function [Filtering], fwp.fwpmprovidercontextenum1_func, fwpmu/FwpmProviderContextEnum1
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
 - FwpmProviderContextEnum1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmProviderContextEnum1 function


## -description


The <b>FwpmProviderContextEnum1</b> function returns the next page of results from the provider context enumerator.
<div class="alert"><b>Note</b>  <b>FwpmProviderContextEnum1</b> is the specific implementation of FwpmProviderContextEnum used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/6c86d858-69f4-41bc-8e08-53c88d124879">FwpmProviderContextEnum2</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/a086c9b3-5cec-4cea-9224-ba423302eba8">FwpmProviderContextEnum0</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for a provider context enumeration created by a call to <a href="https://msdn.microsoft.com/3b660e3a-fba6-4466-aa82-eb90c27ae004">FwpmProviderContextCreateEnumHandle0</a>.


### -param numEntriesRequested [in]

Type: <b>UINT32</b>

The number of provider context objects requested.


### -param entries [out]

Type: <b><a href="https://msdn.microsoft.com/34727579-9baf-4d50-b973-e864ddf651b0">FWPM_PROVIDER_CONTEXT1</a>***</b>

The returned provider context objects.


### -param numEntriesReturned [out]

Type: <b>UINT32*</b>

The number of provider context objects returned.


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
The provider contexts were enumerated successfully.

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



If the <i>numEntriesReturned</i> is less than the <i>numEntriesRequested</i>, the enumeration is exhausted. 

The returned array of entries (but not the individual entries themselves) must be freed by a call to <a href="https://msdn.microsoft.com/ba9f8c1e-f75c-4bf0-b68b-e21a358575fc">FwpmFreeMemory0</a>.

A subsequent call using the same enumeration handle will return the next set of items following those in the last output buffer.

<b>FwpmProviderContextEnum1</b> works on a snapshot of the provider contexts taken at the time the enumeration handle was created.




## -see-also




<a href="https://msdn.microsoft.com/34727579-9baf-4d50-b973-e864ddf651b0">FWPM_PROVIDER_CONTEXT1</a>



<a href="https://msdn.microsoft.com/3b660e3a-fba6-4466-aa82-eb90c27ae004">FwpmProviderContextCreateEnumHandle0</a>
 

 

