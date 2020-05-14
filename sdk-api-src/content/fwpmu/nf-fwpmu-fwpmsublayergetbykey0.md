---
UID: NF:fwpmu.FwpmSubLayerGetByKey0
title: FwpmSubLayerGetByKey0 function (fwpmu.h)
description: Retrieves a sublayer by its key.
helpviewer_keywords: ["FwpmSubLayerGetByKey0","FwpmSubLayerGetByKey0 function [Filtering]","fwp.fwpmsublayergetbykey0_func","fwpmu/FwpmSubLayerGetByKey0"]
old-location: fwp\fwpmsublayergetbykey0_func.htm
tech.root: fwp
ms.assetid: 3435b4fb-abea-43cc-b1a9-a8bea673d72e
ms.date: 12/05/2018
ms.keywords: FwpmSubLayerGetByKey0, FwpmSubLayerGetByKey0 function [Filtering], fwp.fwpmsublayergetbykey0_func, fwpmu/FwpmSubLayerGetByKey0
f1_keywords:
- fwpmu/FwpmSubLayerGetByKey0
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
- FwpmSubLayerGetByKey0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FwpmSubLayerGetByKey0 function


## -description


The <b>FwpmSubLayerGetByKey0</b> function retrieves a sublayer by its key.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param key [in]

Type: <b>const GUID*</b>

Unique identifier of  the sublayer. This is the same GUID that was specified when the application called <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsublayeradd0">FwpmSubLayerAdd0</a>.


### -param subLayer [out]

Type: [FWPM_SUBLAYER0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)**</b>

The sublayer information.


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
The sublayer was retrieved successfully.

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



The caller must free the returned object by a call to <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

The caller needs <a href="https://docs.microsoft.com/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> access to the sublayer. See <a href="https://docs.microsoft.com/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmSubLayerGetByKey0</b> is a specific implementation of FwpmSubLayerGetByKey. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




[FWPM_SUBLAYER0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)



<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsublayeradd0">FwpmSubLayerAdd0</a>
 

 

