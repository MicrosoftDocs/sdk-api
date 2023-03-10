---
UID: NF:fwpmu.IPsecSaContextSetSpi0
title: IPsecSaContextSetSpi0 function (fwpmu.h)
description: Sets the security parameters index (SPI) for a security association (SA) context.
helpviewer_keywords: ["IPsecSaContextSetSpi0","IPsecSaContextSetSpi0 function [Filtering]","fwp.ipsecsacontextsetspi0","fwpmu/IPsecSaContextSetSpi0"]
old-location: fwp\ipsecsacontextsetspi0.htm
tech.root: fwp
ms.assetid: 32812702-e27e-4671-a248-60cc73ce8497
ms.date: 12/05/2018
ms.keywords: IPsecSaContextSetSpi0, IPsecSaContextSetSpi0 function [Filtering], fwp.ipsecsacontextsetspi0, fwpmu/IPsecSaContextSetSpi0
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
 - IPsecSaContextSetSpi0
 - fwpmu/IPsecSaContextSetSpi0
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
 - IPsecSaContextSetSpi0
---

# IPsecSaContextSetSpi0 function


## -description

The <b>IPsecSaContextSetSpi0</b> function sets the security parameters index (SPI) for a security association (SA) context.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

A runtime identifier for the SA context. This identifier was received from the system when the application called <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate1">IPsecSaContextCreate1</a>.

### -param getSpi [in]

Type: [IPSEC_GETSPI1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_getspi1)*</b>

The inbound IPsec traffic.

### -param inboundSpi [in]

Type: <b>IPSEC_SA_SPI</b>

The inbound SA SPI. The <b>IPSEC_SA_SPI</b> data type maps to the <b>UINT32</b> data type.

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
The SPI for the IPsec SA context was set successfully.

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

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD</a> access to the IPsec security associations database. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>IPsecSaContextSetSpi0</b> is a specific implementation of IPsecSaContextSetSpi. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IPSEC_GETSPI1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_getspi1)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate1">IPsecSaContextCreate1</a>