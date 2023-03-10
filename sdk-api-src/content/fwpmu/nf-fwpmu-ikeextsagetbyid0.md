---
UID: NF:fwpmu.IkeextSaGetById0
title: IkeextSaGetById0 function (fwpmu.h)
description: Retrieves an IKE/AuthIP security association (SA) from the database. (IkeextSaGetById0)
helpviewer_keywords: ["IkeextSaGetById0","IkeextSaGetById0 function [Filtering]","fwp.ikeextsagetbyid0","fwpmu/IkeextSaGetById0"]
old-location: fwp\ikeextsagetbyid0.htm
tech.root: fwp
ms.assetid: c500f7d1-ce8f-4a4e-9f09-c37116ef9ab3
ms.date: 12/05/2018
ms.keywords: IkeextSaGetById0, IkeextSaGetById0 function [Filtering], fwp.ikeextsagetbyid0, fwpmu/IkeextSaGetById0
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
 - IkeextSaGetById0
 - fwpmu/IkeextSaGetById0
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
 - IkeextSaGetById0
---

# IkeextSaGetById0 function


## -description

The <b>IkeextSaGetById0</b> function retrieves an IKE/AuthIP security association (SA) from the database.
<div class="alert"><b>Note</b>  <b>IkeextSaGetById0</b> is the specific implementation of IkeextSaGetById used in Windows Vista. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ikeextsagetbyid1">IkeextSaGetById1</a> is available. For Windows 8, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ikeextsagetbyid2">IkeextSaGetById2</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

The SA identifier.

### -param sa [out]

Type: [IKEEXT_SA_DETAILS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details0)**</b>

Address of the SA details.

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
The SA was retrieved successfully.

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

The caller must free <i>sa</i> by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> access to the IKE/AuthIP security associations database. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-ike-functions">IKE/AuthIP Functions</a>



[IKEEXT_SA_DETAILS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details0)



<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>
