---
UID: NF:fwpmu.IPsecSaContextUpdate0
title: IPsecSaContextUpdate0 function (fwpmu.h)
description: Updates an IPsec security association (SA) context.
helpviewer_keywords: ["IPSEC_SA_BUNDLE_UPDATE_FLAGS","IPSEC_SA_BUNDLE_UPDATE_KEY_MODULE_STATE","IPSEC_SA_BUNDLE_UPDATE_MM_SA_ID","IPSEC_SA_BUNDLE_UPDATE_NAP_CONTEXT","IPSEC_SA_BUNDLE_UPDATE_PEER_V4_PRIVATE_ADDRESS","IPSEC_SA_DETAILS_UPDATE_TRAFFIC","IPSEC_SA_DETAILS_UPDATE_UDP_ENCAPSULATION","IPsecSaContextUpdate0","IPsecSaContextUpdate0 function [Filtering]","fwp.ipsecsacontextupdate0","fwpmu/IPsecSaContextUpdate0"]
old-location: fwp\ipsecsacontextupdate0.htm
tech.root: fwp
ms.assetid: ff19c7e6-569e-4bde-9a25-1661d50aea5e
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_BUNDLE_UPDATE_FLAGS, IPSEC_SA_BUNDLE_UPDATE_KEY_MODULE_STATE, IPSEC_SA_BUNDLE_UPDATE_MM_SA_ID, IPSEC_SA_BUNDLE_UPDATE_NAP_CONTEXT, IPSEC_SA_BUNDLE_UPDATE_PEER_V4_PRIVATE_ADDRESS, IPSEC_SA_DETAILS_UPDATE_TRAFFIC, IPSEC_SA_DETAILS_UPDATE_UDP_ENCAPSULATION, IPsecSaContextUpdate0, IPsecSaContextUpdate0 function [Filtering], fwp.ipsecsacontextupdate0, fwpmu/IPsecSaContextUpdate0
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
 - IPsecSaContextUpdate0
 - fwpmu/IPsecSaContextUpdate0
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
 - IPsecSaContextUpdate0
---

# IPsecSaContextUpdate0 function


## -description

The <b>IPsecSaContextUpdate0</b> function updates an IPsec security association (SA) context.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param flags [in]

Type: <b>UINT32</b>

Flags indicating the specific field in the [IPSEC_SA_CONTEXT1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_context1) structure that is being updated.

Possible values:

<table>
<tr>
<th>IPsec SA flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_DETAILS_UPDATE_TRAFFIC"></a><a id="ipsec_sa_details_update_traffic"></a><dl>
<dt><b>IPSEC_SA_DETAILS_UPDATE_TRAFFIC</b></dt>
</dl>
</td>
<td width="60%">
Updates the [IPSEC_SA_DETAILS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1) structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_DETAILS_UPDATE_UDP_ENCAPSULATION"></a><a id="ipsec_sa_details_update_udp_encapsulation"></a><dl>
<dt><b>IPSEC_SA_DETAILS_UPDATE_UDP_ENCAPSULATION</b></dt>
</dl>
</td>
<td width="60%">
Updates the [IPSEC_SA_DETAILS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1) structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_UPDATE_FLAGS"></a><a id="ipsec_sa_bundle_update_flags"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_UPDATE_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
Updates the [IPSEC_SA_BUNDLE1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_UPDATE_NAP_CONTEXT"></a><a id="ipsec_sa_bundle_update_nap_context"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_UPDATE_NAP_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Updates the [IPSEC_SA_BUNDLE1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_UPDATE_KEY_MODULE_STATE"></a><a id="ipsec_sa_bundle_update_key_module_state"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_UPDATE_KEY_MODULE_STATE</b></dt>
</dl>
</td>
<td width="60%">
Updates the [IPSEC_SA_BUNDLE1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_UPDATE_PEER_V4_PRIVATE_ADDRESS"></a><a id="ipsec_sa_bundle_update_peer_v4_private_address"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_UPDATE_PEER_V4_PRIVATE_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Updates the [IPSEC_SA_BUNDLE1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_UPDATE_MM_SA_ID"></a><a id="ipsec_sa_bundle_update_mm_sa_id"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_UPDATE_MM_SA_ID</b></dt>
</dl>
</td>
<td width="60%">
Updates the [IPSEC_SA_BUNDLE1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) structure.

</td>
</tr>
</table>

### -param newValues [in]

Type: [IPSEC_SA_CONTEXT1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_context1)*</b>

An inbound and outbound SA pair.

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
The IPsec SA context was updated successfully.

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

<b>IPsecSaContextUpdate0</b> is a specific implementation of IPsecSaContextUpdate. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IPSEC_SA_CONTEXT1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_context1)