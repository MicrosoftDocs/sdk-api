---
UID: NF:fwpmu.IPsecSaContextEnum0
title: IPsecSaContextEnum0 function
author: windows-sdk-content
description: Returns the next page of results from the IPsec security association (SA) context enumerator.
old-location: fwp\ipsecsacontextenum0.htm
tech.root: fwp
ms.assetid: 67ef4ec6-904b-4b15-a38f-a708448a8646
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IPsecSaContextEnum0, IPsecSaContextEnum0 function [Filtering], fwp.ipsecsacontextenum0, fwpmu/IPsecSaContextEnum0
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
 - IPsecSaContextEnum0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPsecSaContextEnum0 function


## -description


The <b>IPsecSaContextEnum0</b> function returns the next page of results from the IPsec security association (SA) context enumerator.
<div class="alert"><b>Note</b>  <b>IPsecSaContextEnum0</b> is the specific implementation of IPsecSaContextEnum used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/941db3ea-8b3c-47fd-9264-3e76a3d13e87">IPsecSaContextEnum1</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for an SA context enumeration returned by <a href="https://msdn.microsoft.com/ce4340df-e4e0-48ca-b827-2216803a8a94">IPsecSaContextCreateEnumHandle0</a>.


### -param numEntriesRequested [in]

Type: <b>UINT32</b>

Number of SA contexts requested.


### -param entries [out]

Type: <b><a href="https://msdn.microsoft.com/1cf191f0-5052-40f6-8665-747ae3f38fb1">IPSEC_SA_CONTEXT0</a>***</b>

Addresses of the enumeration entries.


### -param numEntriesReturned [out]

Type: <b>UINT32*</b>

The number of SA contexts returned.


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
The IPsec SA contexts were enumerated successfully.

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




## -see-also




<a href="https://msdn.microsoft.com/1cf191f0-5052-40f6-8665-747ae3f38fb1">IPSEC_SA_CONTEXT0</a>



<a href="https://msdn.microsoft.com/ce4340df-e4e0-48ca-b827-2216803a8a94">IPsecSaContextCreateEnumHandle0</a>
 

 

