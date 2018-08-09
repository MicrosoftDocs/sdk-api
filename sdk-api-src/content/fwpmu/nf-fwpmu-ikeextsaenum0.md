---
UID: NF:fwpmu.IkeextSaEnum0
title: IkeextSaEnum0 function
author: windows-sdk-content
description: Returns the next page of results from the IKE/AuthIP security association (SA) enumerator.
old-location: fwp\ikeextsaenum0.htm
old-project: fwp
ms.assetid: a38e266d-2155-4dd4-b12e-5f1a40ca776e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IkeextSaEnum0, IkeextSaEnum0 function [Filtering], fwp.ikeextsaenum0, fwpmu/IkeextSaEnum0
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - IkeextSaEnum0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# IkeextSaEnum0 function


## -description


The <b>IkeextSaEnum0</b> function returns the next page of results from the IKE/AuthIP security association (SA) enumerator.
<div class="alert"><b>Note</b>  <b>IkeextSaEnum0</b> is the specific implementation of IkeextSaEnum used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/245448b0-f7bb-4890-80c0-04ddc90c96f2">IkeextSaEnum1</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/890e6521-69c1-4cb6-ba64-4fe14cb0dffe">IkeextSaEnum2</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for an IKE/AuthIP SA enumeration. Call <a href="https://msdn.microsoft.com/c72ec488-0721-406e-8ca0-6a34873e2683">IkeextSaCreateEnumHandle0</a> to obtain an enumeration handle.


### -param numEntriesRequested [in]

Type: <b>UINT32</b>

Number of enumeration entries requested.


### -param entries [out]

Type: <b><a href="https://msdn.microsoft.com/63d33420-9ae5-4b82-a5f9-469cc5652d59">IKEEXT_SA_DETAILS0</a>***</b>

Addresses of the enumeration entries.


### -param numEntriesReturned [out]

Type: <b>UINT32*</b>

The number of enumeration entries returned.


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
The SAs were enumerated successfully.

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

<b>IkeextSaEnum0</b> works on a snapshot of the SAs taken at the time the enumeration handle was created.




## -see-also




<a href="https://msdn.microsoft.com/df36b6cc-a304-4426-8f16-1bf92fd721e1">IKE/AuthIP Functions</a>



<a href="https://msdn.microsoft.com/63d33420-9ae5-4b82-a5f9-469cc5652d59">IKEEXT_SA_DETAILS0</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>
 

 

