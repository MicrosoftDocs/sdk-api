---
UID: NF:fwpmu.IPsecSaContextGetSpi1
title: IPsecSaContextGetSpi1 function (fwpmu.h)
description: Retrieves the security parameters index (SPI) for a security association (SA) context. (IPsecSaContextGetSpi1)
helpviewer_keywords: ["IPsecSaContextGetSpi1","IPsecSaContextGetSpi1 function [Filtering]","fwp.ipsecsacontextgetspi1","fwpmu/IPsecSaContextGetSpi1"]
old-location: fwp\ipsecsacontextgetspi1.htm
tech.root: fwp
ms.assetid: 623ef4ab-5bcc-4801-ba18-a246da392abe
ms.date: 12/05/2018
ms.keywords: IPsecSaContextGetSpi1, IPsecSaContextGetSpi1 function [Filtering], fwp.ipsecsacontextgetspi1, fwpmu/IPsecSaContextGetSpi1
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
 - IPsecSaContextGetSpi1
 - fwpmu/IPsecSaContextGetSpi1
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
 - IPsecSaContextGetSpi1
---

# IPsecSaContextGetSpi1 function


## -description

The <b>IPsecSaContextGetSpi1</b> function retrieves the security parameters index (SPI) for a security association (SA) context.
<div class="alert"><b>Note</b>  <b>IPsecSaContextGetSpi1</b> is the specific implementation of IPsecSaContextGetSpi used in Windows 7 and later. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextgetspi0">IPsecSaContextGetSpi0</a> is available.</div><div> </div>

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

### -param inboundSpi [out]

Type: <b>IPSEC_SA_SPI*</b>

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
The SPI for the IPsec SA context was retrieved successfully.

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

## -see-also

[IPSEC_GETSPI1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_getspi1)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreate0">IPsecSaContextCreate0</a>
