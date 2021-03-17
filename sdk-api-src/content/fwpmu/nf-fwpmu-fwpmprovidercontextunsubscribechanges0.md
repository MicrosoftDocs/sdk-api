---
UID: NF:fwpmu.FwpmProviderContextUnsubscribeChanges0
title: FwpmProviderContextUnsubscribeChanges0 function (fwpmu.h)
description: Is used to cancel a provider context change subscription and stop receiving change notifications.
helpviewer_keywords: ["FwpmProviderContextUnsubscribeChanges0","FwpmProviderContextUnsubscribeChanges0 function [Filtering]","fwp.fwpmprovidercontextunsubscribechanges0_func","fwpmu/FwpmProviderContextUnsubscribeChanges0"]
old-location: fwp\fwpmprovidercontextunsubscribechanges0_func.htm
tech.root: fwp
ms.assetid: 15c24c24-4aba-4570-aad2-56f8748c03e7
ms.date: 12/05/2018
ms.keywords: FwpmProviderContextUnsubscribeChanges0, FwpmProviderContextUnsubscribeChanges0 function [Filtering], fwp.fwpmprovidercontextunsubscribechanges0_func, fwpmu/FwpmProviderContextUnsubscribeChanges0
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
 - FwpmProviderContextUnsubscribeChanges0
 - fwpmu/FwpmProviderContextUnsubscribeChanges0
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
 - FwpmProviderContextUnsubscribeChanges0
---

# FwpmProviderContextUnsubscribeChanges0 function


## -description

The <b>FwpmProviderContextUnsubscribeChanges0</b> function is used to cancel a provider context change subscription and stop receiving change notifications.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param changeHandle [in]

Type: <b>HANDLE</b>

Handle of the subscribed change notification. This is the handle returned by <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0">FwpmProviderContextSubscribeChanges0</a>.

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
The subscription was deleted successfully.

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

If the callback is currently being invoked, this function will not return until it completes. Thus, when calling this function, you must not hold any locks that the callback may also try to acquire lest you deadlock. 

It is not necessary to unsubscribe before closing a session; all subscriptions are automatically canceled when the subscribing session terminates.

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

<b>FwpmProviderContextUnsubscribeChanges0</b> is a specific implementation of FwpmProviderContextUnsubscribeChanges. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0">FwpmProviderContextSubscribeChanges0</a>