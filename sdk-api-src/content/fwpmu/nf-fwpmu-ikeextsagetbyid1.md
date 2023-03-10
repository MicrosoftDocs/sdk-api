---
UID: NF:fwpmu.IkeextSaGetById1
title: IkeextSaGetById1 function (fwpmu.h)
description: Retrieves an IKE/AuthIP security association (SA) from the database. (IkeextSaGetById1)
helpviewer_keywords: ["IkeextSaGetById1","IkeextSaGetById1 function [Filtering]","fwp.ikeextsagetbyid1","fwpmu/IkeextSaGetById1"]
old-location: fwp\ikeextsagetbyid1.htm
tech.root: fwp
ms.assetid: 99861d5e-31df-47ef-a922-a1720b17c70e
ms.date: 12/05/2018
ms.keywords: IkeextSaGetById1, IkeextSaGetById1 function [Filtering], fwp.ikeextsagetbyid1, fwpmu/IkeextSaGetById1
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
 - IkeextSaGetById1
 - fwpmu/IkeextSaGetById1
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
 - IkeextSaGetById1
---

# IkeextSaGetById1 function


## -description

The <b>IkeextSaGetById1</b> function retrieves an IKE/AuthIP security association (SA) from the database. 
<div class="alert"><b>Note</b>  <b>IkeextSaGetById1</b> is the specific implementation of IkeextSaGetById used in Windows 7. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ikeextsagetbyid2">IkeextSaGetById2</a> is available. For Windows Vista, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ikeextsagetbyid0">IkeextSaGetById0</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

The SA identifier.

### -param saLookupContext [in, optional]

Type: <b>GUID*</b>

Optional pointer to the SA lookup context propagated from the SA to data connections flowing over that SA. It is made available to any application that queries socket security properties using the Winsock API <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity">WSAQuerySocketSecurity</a> function, allowing the application to obtain detailed IPsec authentication information for its connection.

### -param sa [out]

Type: [IKEEXT_SA_DETAILS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details1)**</b>

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



[IKEEXT_SA_DETAILS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details1)



<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>
