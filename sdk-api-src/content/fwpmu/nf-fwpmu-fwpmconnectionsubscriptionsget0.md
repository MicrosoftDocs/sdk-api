---
UID: NF:fwpmu.FwpmConnectionSubscriptionsGet0
title: FwpmConnectionSubscriptionsGet0 function (fwpmu.h)
description: Retrieves an array of all the current connection object change notification subscriptions.
helpviewer_keywords: ["FwpmConnectionSubscriptionsGet0","FwpmConnectionSubscriptionsGet0 function [Filtering]","fwp.fwpmconnectionsubscriptionsget0","fwpmu/FwpmConnectionSubscriptionsGet0"]
old-location: fwp\fwpmconnectionsubscriptionsget0.htm
tech.root: fwp
ms.assetid: fc6c94be-9c2f-4b32-9cf5-4af33b8f1c97
ms.date: 12/05/2018
ms.keywords: FwpmConnectionSubscriptionsGet0, FwpmConnectionSubscriptionsGet0 function [Filtering], fwp.fwpmconnectionsubscriptionsget0, fwpmu/FwpmConnectionSubscriptionsGet0
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fwpuclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmConnectionSubscriptionsGet0
 - fwpmu/FwpmConnectionSubscriptionsGet0
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
 - FwpmConnectionSubscriptionsGet0
---

# FwpmConnectionSubscriptionsGet0 function


## -description

The <b>FwpmConnectionSubscriptionsGet0</b> function retrieves an array of all the current connection object change notification subscriptions.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param entries [out]

Type: [FWPM_CONNECTION_SUBSCRIPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)***</b>

The current connection object notification subscriptions.

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

## -see-also

[FWPM_CONNECTION_SUBSCRIPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)