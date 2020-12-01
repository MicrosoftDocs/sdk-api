---
UID: NF:fwpmu.IPsecKeyManagersGet0
title: IPsecKeyManagersGet0 function (fwpmu.h)
description: Returns a list of current Trusted Intermediary Agents (TIAs).
helpviewer_keywords: ["IPsecKeyManagersGet0","IPsecKeyManagersGet0 function [Filtering]","fwp.ipseckeymanagersget0","fwpmu/IPsecKeyManagersGet0"]
old-location: fwp\ipseckeymanagersget0.htm
tech.root: fwp
ms.assetid: 5456C126-DF5F-472D-A3A2-37C2C0C1E2FE
ms.date: 12/05/2018
ms.keywords: IPsecKeyManagersGet0, IPsecKeyManagersGet0 function [Filtering], fwp.ipseckeymanagersget0, fwpmu/IPsecKeyManagersGet0
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
 - IPsecKeyManagersGet0
 - fwpmu/IPsecKeyManagersGet0
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
 - IPsecKeyManagersGet0
---

# IPsecKeyManagersGet0 function


## -description

The <b>IPsecKeyManagersGet0</b> function returns a list of current Trusted Intermediary Agents (TIAs).

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param entries [out]

Type: <b><a href="/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0">IPSEC_KEY_MANAGER0</a>***</b>

All of the current TIAs.

### -param numEntries [out]

Type: <b>UINT32*</b>

The number of entries returned.

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
The list of current TIAs was successfully returned.

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

The returned array of entries (but not the individual entries themselves) must be freed by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

## -see-also

<a href="/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0">IPSEC_KEY_MANAGER0</a>



<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>