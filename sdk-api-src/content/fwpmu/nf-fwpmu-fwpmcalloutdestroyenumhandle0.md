---
UID: NF:fwpmu.FwpmCalloutDestroyEnumHandle0
title: FwpmCalloutDestroyEnumHandle0 function (fwpmu.h)
description: Frees a handle returned by FwpmCalloutCreateEnumHandle0.
helpviewer_keywords: ["FwpmCalloutDestroyEnumHandle0","FwpmCalloutDestroyEnumHandle0 function [Filtering]","fwp.fwpmcalloutdestroyenumhandle0_func","fwpmu/FwpmCalloutDestroyEnumHandle0"]
old-location: fwp\fwpmcalloutdestroyenumhandle0_func.htm
tech.root: fwp
ms.assetid: 6aa41eed-b53c-4b35-a45c-88f89086cacc
ms.date: 12/05/2018
ms.keywords: FwpmCalloutDestroyEnumHandle0, FwpmCalloutDestroyEnumHandle0 function [Filtering], fwp.fwpmcalloutdestroyenumhandle0_func, fwpmu/FwpmCalloutDestroyEnumHandle0
f1_keywords:
- fwpmu/FwpmCalloutDestroyEnumHandle0
dev_langs:
- c++
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
- FwpmCalloutDestroyEnumHandle0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FwpmCalloutDestroyEnumHandle0 function


## -description


The <b>FwpmCalloutDestroyEnumHandle0</b> function frees a handle returned by <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0">FwpmCalloutCreateEnumHandle0</a>.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle of a callout enumeration created by a call to <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0">FwpmCalloutCreateEnumHandle0</a>.


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
The enumerator was successfully deleted.

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
A Windows Filtering Platform (WFP) specific error. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

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



<b>FwpmCalloutDestroyEnumHandle0</b> is a specific implementation of FwpmCalloutDestroyEnumHandle. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0">FwpmCalloutCreateEnumHandle0</a>
 

 

