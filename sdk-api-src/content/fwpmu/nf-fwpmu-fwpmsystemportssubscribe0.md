---
UID: NF:fwpmu.FwpmSystemPortsSubscribe0
title: FwpmSystemPortsSubscribe0 function (fwpmu.h)
description: Is used to request the delivery of notifications regarding a particular system port.
helpviewer_keywords: ["FwpmSystemPortsSubscribe0","FwpmSystemPortsSubscribe0 function [Filtering]","fwp.fwpmsystemportssubscribe0","fwpmu/FwpmSystemPortsSubscribe0"]
old-location: fwp\fwpmsystemportssubscribe0.htm
tech.root: fwp
ms.assetid: e0eecf0e-e6b2-4df9-8a8e-766ee5c8189f
ms.date: 12/05/2018
ms.keywords: FwpmSystemPortsSubscribe0, FwpmSystemPortsSubscribe0 function [Filtering], fwp.fwpmsystemportssubscribe0, fwpmu/FwpmSystemPortsSubscribe0
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
 - FwpmSystemPortsSubscribe0
 - fwpmu/FwpmSystemPortsSubscribe0
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
 - FwpmSystemPortsSubscribe0
---

# FwpmSystemPortsSubscribe0 function


## -description

The <b>FwpmSystemPortsSubscribe0</b> function  is used to request the delivery of notifications regarding a particular system port.

## -parameters

### -param engineHandle [in, optional]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param reserved

Type: <b>void*</b>

Reserved.

### -param callback [in]

Type: <b><a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_system_ports_callback0">FWPM_SYSTEM_PORTS_CALLBACK0</a></b>

Function pointer that will be invoked when a notification is ready for delivery.

### -param context [in, optional]

Type: <b>void*</b>

Optional context pointer. This pointer is passed to the <i>callback</i> function along with details of the system port.

### -param sysPortsHandle [out]

Type: <b>HANDLE*</b>

Handle to the newly created subscription.

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
The subscription was created successfully.

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

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

<b>FwpmSystemPortsSubscribe0</b> is a specific implementation of FwpmSystemPortsSubscribe. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_system_ports_callback0">FWPM_SYSTEM_PORTS_CALLBACK0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsunsubscribe0">FwpmSystemPortsUnsubscribe0</a>