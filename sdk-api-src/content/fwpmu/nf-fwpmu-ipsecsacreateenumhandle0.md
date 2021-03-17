---
UID: NF:fwpmu.IPsecSaCreateEnumHandle0
title: IPsecSaCreateEnumHandle0 function (fwpmu.h)
description: Creates a handle used to enumerate a set of Internet Protocol Security (IPsec) security association (SA) objects.
helpviewer_keywords: ["IPsecSaCreateEnumHandle0","IPsecSaCreateEnumHandle0 function [Filtering]","fwp.ipsecsacreateenumhandle0_func","fwpmu/IPsecSaCreateEnumHandle0"]
old-location: fwp\ipsecsacreateenumhandle0_func.htm
tech.root: fwp
ms.assetid: 473935d9-362f-417c-a366-f683d97d9a18
ms.date: 12/05/2018
ms.keywords: IPsecSaCreateEnumHandle0, IPsecSaCreateEnumHandle0 function [Filtering], fwp.ipsecsacreateenumhandle0_func, fwpmu/IPsecSaCreateEnumHandle0
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
 - IPsecSaCreateEnumHandle0
 - fwpmu/IPsecSaCreateEnumHandle0
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
 - IPsecSaCreateEnumHandle0
---

# IPsecSaCreateEnumHandle0 function


## -description

The <b>IPsecSaCreateEnumHandle0</b> function creates a handle used to enumerate a set of Internet Protocol Security (IPsec) security association (SA) objects.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumTemplate [in, optional]

Type: [IPSEC_SA_ENUM_TEMPLATE0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)*</b>

Template to selectively restrict the enumeration.

### -param enumHandle [out]

Type: <b>HANDLE*</b>

Handle of the newly created enumeration.

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
The enumeration was created successfully.

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

If <i>enumTemplate</i> is <b>NULL</b>, all IPsec SA objects are returned.

The caller must call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsadestroyenumhandle0">IPsecSaDestroyEnumHandle0</a> to free the returned handle.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> and <b>FWPM_ACTRL_ENUM</b> access to the IPsec security associations database. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>IPsecSaCreateEnumHandle0</b> is a specific implementation of IPsecSaCreateEnumHandle. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IPSEC_SA_ENUM_TEMPLATE0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsadestroyenumhandle0">IPsecSaDestroyEnumHandle0</a>