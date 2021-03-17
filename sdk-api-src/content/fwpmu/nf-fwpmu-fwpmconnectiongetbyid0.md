---
UID: NF:fwpmu.FwpmConnectionGetById0
title: FwpmConnectionGetById0 function (fwpmu.h)
description: Retrieves a connection object.
helpviewer_keywords: ["FwpmConnectionGetById0","FwpmConnectionGetById0 function [Filtering]","fwp.fwpmconnectiongetbyid0","fwpmu/FwpmConnectionGetById0"]
old-location: fwp\fwpmconnectiongetbyid0.htm
tech.root: fwp
ms.assetid: 630f513b-49c9-4d3a-a5e2-7ea6b940d333
ms.date: 12/05/2018
ms.keywords: FwpmConnectionGetById0, FwpmConnectionGetById0 function [Filtering], fwp.fwpmconnectiongetbyid0, fwpmu/FwpmConnectionGetById0
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmConnectionGetById0
 - fwpmu/FwpmConnectionGetById0
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
 - FwpmConnectionGetById0
---

# FwpmConnectionGetById0 function


## -description

The <b>FwpmConnectionGetById0</b> function retrieves a connection object.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

The run-time identifier for the connection.

### -param connection [out]

Type: [FWPM_CONNECTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection0)**</b>

The connection information.

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
The connection object was retrieved successfully.

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

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> access to the provider context. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

## -see-also

[FWPM_CONNECTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection0)