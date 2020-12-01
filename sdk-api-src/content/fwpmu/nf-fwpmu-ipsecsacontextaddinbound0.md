---
UID: NF:fwpmu.IPsecSaContextAddInbound0
title: IPsecSaContextAddInbound0 function (fwpmu.h)
description: The IPsecSaContextAddInbound0 function adds an inbound IPsec security association (SA) bundle to an existing SA context.Note  IPsecSaContextAddInbound0 is the specific implementation of IPsecSaContextAddInbound used in Windows Vista.
helpviewer_keywords: ["IPsecSaContextAddInbound0","IPsecSaContextAddInbound0 function [Filtering]","fwp.ipsecsacontextaddinbound0","fwpmu/IPsecSaContextAddInbound0"]
old-location: fwp\ipsecsacontextaddinbound0.htm
tech.root: fwp
ms.assetid: e0798bcb-847d-481e-b9f0-b18c0bbad22c
ms.date: 12/05/2018
ms.keywords: IPsecSaContextAddInbound0, IPsecSaContextAddInbound0 function [Filtering], fwp.ipsecsacontextaddinbound0, fwpmu/IPsecSaContextAddInbound0
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
 - IPsecSaContextAddInbound0
 - fwpmu/IPsecSaContextAddInbound0
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
 - IPsecSaContextAddInbound0
---

# IPsecSaContextAddInbound0 function


## -description

The <b>IPsecSaContextAddInbound0</b> function adds an inbound IPsec security association (SA) bundle to an existing SA context.
<div class="alert"><b>Note</b>  <b>IPsecSaContextAddInbound0</b> is the specific implementation of IPsecSaContextAddInbound used in Windows Vista. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextaddinbound1">IPsecSaContextAddInbound1</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

Identifier for the existing IPsec SA context. This is the value returned in the <i>id</i> parameter by the call to  <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate0">IPsecSaContextCreate0</a>.

### -param inboundBundle [in]

Type: [IPSEC_SA_BUNDLE0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle0)*</b>

The inbound IPsec SA bundle to be added to the SA context.

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
The IPsec SA bundle was successfully added to the SA context.

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

## -see-also

[IPSEC_SA_BUNDLE0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate0">IPsecSaContextCreate0</a>