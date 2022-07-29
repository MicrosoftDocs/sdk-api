---
UID: NF:fwpmu.FwpmFilterGetByKey0
title: FwpmFilterGetByKey0 function (fwpmu.h)
description: Retrieves a filter object. (FwpmFilterGetByKey0)
helpviewer_keywords: ["FwpmFilterGetByKey0","FwpmFilterGetByKey0 function [Filtering]","fwp.fwpmfiltergetbykey0_func","fwpmu/FwpmFilterGetByKey0"]
old-location: fwp\fwpmfiltergetbykey0_func.htm
tech.root: fwp
ms.assetid: 5ab0942c-aee2-44f9-9e7f-568405131691
ms.date: 12/05/2018
ms.keywords: FwpmFilterGetByKey0, FwpmFilterGetByKey0 function [Filtering], fwp.fwpmfiltergetbykey0_func, fwpmu/FwpmFilterGetByKey0
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmFilterGetByKey0
 - fwpmu/FwpmFilterGetByKey0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmFilterGetByKey0
---

# FwpmFilterGetByKey0 function


## -description

The <b>FwpmFilterGetByKey0</b> function retrieves a filter object.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param key [in]

Type: <b>const GUID*</b>

Unique identifier of the filter. This GUID was specified in the <b>filterKey</b> member of the <i>filter</i> parameter when the application called <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfilteradd0">FwpmFilterAdd0</a> for this object.

### -param filter [out]

Type: [FWPM_FILTER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)**</b>

The filter information.

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
The filter was retrieved successfully.

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
A Windows Filtering Platform (WFP) specific error. See <a href="/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

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

The caller must free the returned object by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> access to the filter. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmFilterGetByKey0</b> is a specific implementation of FwpmFilterGetByKey. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_FILTER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfilteradd0">FwpmFilterAdd0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfilterdeletebykey0">FwpmFilterDeleteByKey0</a>
