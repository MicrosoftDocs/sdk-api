---
UID: NF:fwpmu.IPsecKeyManagerAddAndRegister0
title: IPsecKeyManagerAddAndRegister0 function (fwpmu.h)
description: Registers a Trusted Intermediary Agent (TIA) with IPsec.
helpviewer_keywords: ["IPsecKeyManagerAddAndRegister0","IPsecKeyManagerAddAndRegister0 function [Filtering]","fwp.ipseckeymanageraddandregister0","fwpmu/IPsecKeyManagerAddAndRegister0"]
old-location: fwp\ipseckeymanageraddandregister0.htm
tech.root: fwp
ms.assetid: 9606A611-6C55-4548-B9C4-688580338F08
ms.date: 12/05/2018
ms.keywords: IPsecKeyManagerAddAndRegister0, IPsecKeyManagerAddAndRegister0 function [Filtering], fwp.ipseckeymanageraddandregister0, fwpmu/IPsecKeyManagerAddAndRegister0
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
 - IPsecKeyManagerAddAndRegister0
 - fwpmu/IPsecKeyManagerAddAndRegister0
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
 - IPsecKeyManagerAddAndRegister0
---

# IPsecKeyManagerAddAndRegister0 function


## -description

The <b>IPsecKeyManagerAddAndRegister0</b> function registers a Trusted Intermediary Agent (TIA) with IPsec.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param keyManager [in]

Type: <b>const <a href="/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0">IPSEC_KEY_MANAGER0</a>*</b>

The set of key management callbacks which IPsec will invoke.

### -param keyManagerCallbacks [in]

Type: <b>const <a href="/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0">IPSEC_KEY_MANAGER_CALLBACKS0</a>*</b>

The set of callbacks which should be invoked by IPsec at various stages of SA negotiation.

### -param keyMgmtHandle [out]

Type: <b>HANDLE*</b>

Address of the newly created registration.

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
The TIA was successfully registered.

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
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_ALREADY_EXISTS</b></dt>
<dt>0x80320009L</dt>
</dl>
</td>
<td width="60%">
The TIA was not registered successfully because another TIA has already been registered to dictate keys.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_INVALID_INTERVAL</b></dt>
<dt>0x80320021L</dt>
</dl>
</td>
<td width="60%">
The TIA was not registered successfully because <i>keyDictationTimeoutHint</i> exceeded the maximum allowed value of 10 seconds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_CANNOT_INSTALL</b></dt>
<dt>0x80090307L</dt>
</dl>
</td>
<td width="60%">
The TIA was not registered successfully because the binary image has not set the <b>IMAGE_DLLCHARACTERISTICS_FORCE_INTEGRITY</b> property.

</td>
</tr>
</table>

## -remarks

If the <b>IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY</b> flag is set for <b>keyManager</b>, all three callback members of <b>keyManagerCallbacks</b> must be specified; otherwise, only the <b>keyNotify</b> callback should be specified

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

## -see-also

<a href="/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0">IPSEC_KEY_MANAGER0</a>



<a href="/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0">IPSEC_KEY_MANAGER_CALLBACKS0</a>



<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>