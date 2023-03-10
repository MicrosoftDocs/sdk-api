---
UID: NF:fwpmu.IPsecSaContextAddInbound1
title: IPsecSaContextAddInbound1 function (fwpmu.h)
description: The IPsecSaContextAddInbound1 function adds an inbound IPsec security association (SA) bundle to an existing SA context.Note  IPsecSaContextAddInbound1 is the specific implementation of IPsecSaContextAddInbound used in Windows 7 and later.
helpviewer_keywords: ["IPsecSaContextAddInbound1","IPsecSaContextAddInbound1 function [Filtering]","fwp.ipsecsacontextaddinbound1","fwpmu/IPsecSaContextAddInbound1"]
old-location: fwp\ipsecsacontextaddinbound1.htm
tech.root: fwp
ms.assetid: a6717ff9-41f9-4cbc-9493-b9d80a137571
ms.date: 12/05/2018
ms.keywords: IPsecSaContextAddInbound1, IPsecSaContextAddInbound1 function [Filtering], fwp.ipsecsacontextaddinbound1, fwpmu/IPsecSaContextAddInbound1
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
 - IPsecSaContextAddInbound1
 - fwpmu/IPsecSaContextAddInbound1
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
 - IPsecSaContextAddInbound1
---

# IPsecSaContextAddInbound1 function


## -description

The <b>IPsecSaContextAddInbound1</b> function adds an inbound IPsec security association (SA) bundle to an existing SA context.
<div class="alert"><b>Note</b>  <b>IPsecSaContextAddInbound1</b> is the specific implementation of IPsecSaContextAddInbound used in Windows 7 and later. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextaddinbound0">IPsecSaContextAddInbound0</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

Identifier for the existing IPsec SA context. This is the value returned in the <i>id</i> parameter by the call to  <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate1">IPsecSaContextCreate1</a>.

### -param inboundBundle [in]

Type: [IPSEC_SA_BUNDLE1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)*</b>

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

[IPSEC_SA_BUNDLE1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate1">IPsecSaContextCreate1</a>