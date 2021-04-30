---
UID: NF:fwpmu.IPsecDospGetStatistics0
title: IPsecDospGetStatistics0 function (fwpmu.h)
description: The IPsecDospGetStatistics0 function retrieves Internet Protocol Security (IPsec) DoS Protection statistics.
helpviewer_keywords: ["IPsecDospGetStatistics0","IPsecDospGetStatistics0 function [Filtering]","fwp.ipsecdospgetstatistics0","fwpmu/IPsecDospGetStatistics0"]
old-location: fwp\ipsecdospgetstatistics0.htm
tech.root: fwp
ms.assetid: eb71e7c8-403c-4774-bc59-71e4a56ee1c4
ms.date: 12/05/2018
ms.keywords: IPsecDospGetStatistics0, IPsecDospGetStatistics0 function [Filtering], fwp.ipsecdospgetstatistics0, fwpmu/IPsecDospGetStatistics0
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
 - IPsecDospGetStatistics0
 - fwpmu/IPsecDospGetStatistics0
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
 - IPsecDospGetStatistics0
---

# IPsecDospGetStatistics0 function


## -description

The <b>IPsecDospGetStatistics0</b> function retrieves Internet Protocol Security (IPsec) DoS Protection statistics.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param idpStatistics [out]

Type: [IPSEC_DOSP_STATISTICS0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)*</b>

Top-level object of IPsec DoS Protection statistics organization.

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
The IPsec DoS Protection statistics were  successfully returned.

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

This function cannot be called from within a transaction. It will fail with
<b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ_STATS</a> access to the IPsec DoS Protection component. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>IPsecDospGetStatistics0</b> is a specific implementation of IPsecDospGetStatistics. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IPSEC_DOSP_STATISTICS0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)