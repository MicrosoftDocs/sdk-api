---
UID: NF:fwpmu.FwpmSystemPortsGet0
title: FwpmSystemPortsGet0 function (fwpmu.h)
description: Retrieves an array of all of the system port types.
helpviewer_keywords: ["FwpmSystemPortsGet0","FwpmSystemPortsGet0 function [Filtering]","fwp.fwpmsystemportsget0","fwpmu/FwpmSystemPortsGet0"]
old-location: fwp\fwpmsystemportsget0.htm
tech.root: fwp
ms.assetid: 675b1078-8f8e-4a97-aa01-fbf8fbe2b50f
ms.date: 12/05/2018
ms.keywords: FwpmSystemPortsGet0, FwpmSystemPortsGet0 function [Filtering], fwp.fwpmsystemportsget0, fwpmu/FwpmSystemPortsGet0
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmSystemPortsGet0
 - fwpmu/FwpmSystemPortsGet0
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
 - FwpmSystemPortsGet0
---

# FwpmSystemPortsGet0 function


## -description

The <b>FwpmSystemPortsGet0</b> function  retrieves an array of all of the system port types.

## -parameters

### -param engineHandle [in, optional]

Type: <b>HANDLE</b>

Optional handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param sysPorts [out]

Type: [FWPM_SYSTEM_PORTS0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)**</b>

The array of system port types.

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
The subscriptions were retrieved successfully.

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

The returned array (but not the individual entries in the array) must be freed through a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

<b>FwpmSystemPortsGet0</b> is a specific implementation of FwpmSystemPortsGet. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_SYSTEM_PORTS0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)