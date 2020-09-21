---
UID: NF:fwpmu.FwpmIPsecTunnelDeleteByKey0
title: FwpmIPsecTunnelDeleteByKey0 function (fwpmu.h)
description: Removes an Internet Protocol Security (IPsec) tunnel mode policy from the system.
helpviewer_keywords: ["FwpmIPsecTunnelDeleteByKey0","FwpmIPsecTunnelDeleteByKey0 function [Filtering]","fwp.fwpmipsectunneldeletebykey0","fwpmu/FwpmIPsecTunnelDeleteByKey0"]
old-location: fwp\fwpmipsectunneldeletebykey0.htm
tech.root: fwp
ms.assetid: cbef853e-0d6e-420b-84a9-640f56614fe7
ms.date: 12/05/2018
ms.keywords: FwpmIPsecTunnelDeleteByKey0, FwpmIPsecTunnelDeleteByKey0 function [Filtering], fwp.fwpmipsectunneldeletebykey0, fwpmu/FwpmIPsecTunnelDeleteByKey0
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
 - FwpmIPsecTunnelDeleteByKey0
 - fwpmu/FwpmIPsecTunnelDeleteByKey0
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
 - FwpmIPsecTunnelDeleteByKey0
---

# FwpmIPsecTunnelDeleteByKey0 function


## -description

The <b>FwpmIPsecTunnelDeleteByKey0</b> function removes an Internet Protocol Security (IPsec) tunnel mode policy from the system.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param key [in]

Type: <b>const GUID*</b>

Unique identifier of the IPsec tunnel.  This GUID was specified in the <b>providerContextKey</b> member of the <i>tunnelPolicy</i> parameter of the <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd0">FwpmIPsecTunnelAdd0</a> function.

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
The IPsec tunnel mode policy was successfully deleted.

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

This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

<b>FwpmIPsecTunnelDeleteByKey0</b> is a specific implementation of FwpmIPsecTunnelDeleteByKey. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd0">FwpmIPsecTunnelAdd0</a>