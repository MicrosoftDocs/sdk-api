---
UID: NF:fwpmu.IPsecSaContextDeleteById0
title: IPsecSaContextDeleteById0 function (fwpmu.h)
description: Deletes an IPsec security association (SA) context.
helpviewer_keywords: ["IPsecSaContextDeleteById0","IPsecSaContextDeleteById0 function [Filtering]","fwp.ipsecsacontextdeletebyid0","fwpmu/IPsecSaContextDeleteById0"]
old-location: fwp\ipsecsacontextdeletebyid0.htm
tech.root: fwp
ms.assetid: 4e3b1c5e-3da4-4c6b-aacf-beb90aa96923
ms.date: 12/05/2018
ms.keywords: IPsecSaContextDeleteById0, IPsecSaContextDeleteById0 function [Filtering], fwp.ipsecsacontextdeletebyid0, fwpmu/IPsecSaContextDeleteById0
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
 - IPsecSaContextDeleteById0
 - fwpmu/IPsecSaContextDeleteById0
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
 - IPsecSaContextDeleteById0
---

# IPsecSaContextDeleteById0 function


## -description

The <b>IPsecSaContextDeleteById0</b> function deletes an IPsec security association (SA) context.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

A runtime identifier for the object being removed from the system.  This identifier was received from the system when the application called <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate0">IPsecSaContextCreate0</a>.

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
The IPsec SA context was successfully deleted.

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

This function cannot be called from within a dynamic session. The call will fail with <b>FWP_E_DYNAMIC_SESSION_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about dynamic sessions.

The caller needs <a href="/windows/desktop/SecAuthZ/standard-access-rights">DELETE</a> access to the IPsec security associations database. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>IPsecSaContextDeleteById0</b> is a specific implementation of IPsecSaContextDeleteById. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate0">IPsecSaContextCreate0</a>