---
UID: NF:fwpmu.IPsecSaContextExpire0
title: IPsecSaContextExpire0 function (fwpmu.h)
description: Indicates that an IPsec security association (SA) context should be expired.
helpviewer_keywords: ["IPsecSaContextExpire0","IPsecSaContextExpire0 function [Filtering]","fwp.ipsecsacontextexpire0","fwpmu/IPsecSaContextExpire0"]
old-location: fwp\ipsecsacontextexpire0.htm
tech.root: fwp
ms.assetid: 7e249e61-ba40-4dd9-b675-c3c86e8dd1bf
ms.date: 12/05/2018
ms.keywords: IPsecSaContextExpire0, IPsecSaContextExpire0 function [Filtering], fwp.ipsecsacontextexpire0, fwpmu/IPsecSaContextExpire0
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
 - IPsecSaContextExpire0
 - fwpmu/IPsecSaContextExpire0
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
 - IPsecSaContextExpire0
---

# IPsecSaContextExpire0 function


## -description

The <b>IPsecSaContextExpire0</b> function indicates that an IPsec security association (SA) context should be expired.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

A runtime identifier for SA context. This identifier was received from the system when the application called <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate0">IPsecSaContextCreate0</a>.

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
The IPsec SA context was successfully expired.

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

When an SA context is expired, the corresponding outbound SA gets deleted immediately, whereas the inbound SA deletion is postponed for a minute. This allows the processing of any inbound IPsec protected traffic that may still be on the wire.

The caller needs <a href="/windows/desktop/SecAuthZ/standard-access-rights">DELETE</a> access to the IPsec security associations database. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>IPsecSaContextExpire0</b> is a specific implementation of IPsecSaContextExpire. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate0">IPsecSaContextCreate0</a>