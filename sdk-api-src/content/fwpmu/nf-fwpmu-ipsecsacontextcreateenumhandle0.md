---
UID: NF:fwpmu.IPsecSaContextCreateEnumHandle0
title: IPsecSaContextCreateEnumHandle0 function (fwpmu.h)
description: Creates a handle used to enumerate a set of IPsec security association (SA) context objects.
helpviewer_keywords: ["IPsecSaContextCreateEnumHandle0","IPsecSaContextCreateEnumHandle0 function [Filtering]","fwp.ipsecsacontextcreateenumhandle0","fwpmu/IPsecSaContextCreateEnumHandle0"]
old-location: fwp\ipsecsacontextcreateenumhandle0.htm
tech.root: fwp
ms.assetid: ce4340df-e4e0-48ca-b827-2216803a8a94
ms.date: 12/05/2018
ms.keywords: IPsecSaContextCreateEnumHandle0, IPsecSaContextCreateEnumHandle0 function [Filtering], fwp.ipsecsacontextcreateenumhandle0, fwpmu/IPsecSaContextCreateEnumHandle0
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
 - IPsecSaContextCreateEnumHandle0
 - fwpmu/IPsecSaContextCreateEnumHandle0
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
 - IPsecSaContextCreateEnumHandle0
---

# IPsecSaContextCreateEnumHandle0 function


## -description

The <b>IPsecSaContextCreateEnumHandle0</b> function creates a handle used to enumerate a set of IPsec security association (SA) context objects.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumTemplate [in, optional]

Type: <b>const <a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0">IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</a>*</b>

Template to selectively restrict the enumeration.

### -param enumHandle [out]

Type: <b>HANDLE*</b>

Address of a <b>HANDLE</b> variable. On function return, it contains the handle for SA context enumeration.

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
The enumerator was created successfully.

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

The caller must call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextdestroyenumhandle0">IPsecSaContextDestroyEnumHandle0</a> to free the returned handle.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ENUM</a> and <b>FWPM_ACTRL_READ</b> access to the IPsec security associations database. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>IPsecSaContextCreateEnumHandle0</b> is a specific implementation of IPsecSaContextCreateEnumHandle. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0">IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextdestroyenumhandle0">IPsecSaContextDestroyEnumHandle0</a>