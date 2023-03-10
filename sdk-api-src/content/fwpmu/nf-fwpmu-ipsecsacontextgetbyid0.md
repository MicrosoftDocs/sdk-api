---
UID: NF:fwpmu.IPsecSaContextGetById0
title: IPsecSaContextGetById0 function (fwpmu.h)
description: Retrieves an IPsec security association (SA) context. (IPsecSaContextGetById0)
helpviewer_keywords: ["IPsecSaContextGetById0","IPsecSaContextGetById0 function [Filtering]","fwp.ipsecsacontextgetbyid0","fwpmu/IPsecSaContextGetById0"]
old-location: fwp\ipsecsacontextgetbyid0.htm
tech.root: fwp
ms.assetid: a5bfd0e6-0113-4953-954c-d58e9cda91f0
ms.date: 12/05/2018
ms.keywords: IPsecSaContextGetById0, IPsecSaContextGetById0 function [Filtering], fwp.ipsecsacontextgetbyid0, fwpmu/IPsecSaContextGetById0
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
 - IPsecSaContextGetById0
 - fwpmu/IPsecSaContextGetById0
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
 - IPsecSaContextGetById0
---

# IPsecSaContextGetById0 function


## -description

The <b>IPsecSaContextGetById0</b> function retrieves an IPsec security association (SA) context.
<div class="alert"><b>Note</b>  <b>IPsecSaContextGetById0</b> is the specific implementation of IPsecSaContextGetById used in Windows Vista. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextgetbyid1">IPsecSaContextGetById1</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

A runtime identifier for the SA context. This identifier was received from the system when the application called <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate0">IPsecSaContextCreate0</a>.

### -param saContext [out]

Type: [IPSEC_SA_CONTEXT0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_context0)**</b>

Address of the IPsec SA context.

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
The IPsec SA context was successfully retrieved.

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

The caller must free the returned object, <i>saContext</i>,  by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> access to the IPsec security associations database. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

## -see-also

[IPSEC_SA_CONTEXT0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_context0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate0">IPsecSaContextCreate0</a>
