---
UID: NF:fwpmu.FwpmSubLayerSubscriptionsGet0
title: FwpmSubLayerSubscriptionsGet0 function (fwpmu.h)
description: Retrieves an array of all the current sub-layer change notification subscriptions.
helpviewer_keywords: ["FwpmSubLayerSubscriptionsGet0","FwpmSubLayerSubscriptionsGet0 function [Filtering]","fwp.fwpmsublayersubscriptionsget0_func","fwpmu/FwpmSubLayerSubscriptionsGet0"]
old-location: fwp\fwpmsublayersubscriptionsget0_func.htm
tech.root: fwp
ms.assetid: ca00c768-d8fe-4f61-8b23-2f3a79b4116c
ms.date: 12/05/2018
ms.keywords: FwpmSubLayerSubscriptionsGet0, FwpmSubLayerSubscriptionsGet0 function [Filtering], fwp.fwpmsublayersubscriptionsget0_func, fwpmu/FwpmSubLayerSubscriptionsGet0
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
 - FwpmSubLayerSubscriptionsGet0
 - fwpmu/FwpmSubLayerSubscriptionsGet0
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
 - FwpmSubLayerSubscriptionsGet0
---

# FwpmSubLayerSubscriptionsGet0 function


## -description

The <b>FwpmSubLayerSubscriptionsGet0</b> function retrieves an array of all the current sub-layer change notification subscriptions.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param entries [out]

Type: [FWPM_SUBLAYER_SUBSCRIPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)***</b>

The current sublayer change notification subscriptions.

### -param numEntries [out]

Type: <b>UINT32*</b>

The number of entries returned.

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
The subscriptions were retrieved successfully.

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

The returned array (but not the individual entries in the array) must be freed through a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> access to the sublayer's container. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmSubLayerSubscriptionsGet0</b> is a specific implementation of FwpmSubLayerSubscriptionsGet. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_SUBLAYER_SUBSCRIPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)