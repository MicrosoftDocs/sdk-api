---
UID: NF:fwpmu.FwpmEngineClose0
title: FwpmEngineClose0 function (fwpmu.h)
description: Closes a session to a filter engine.
helpviewer_keywords: ["FwpmEngineClose0","FwpmEngineClose0 function [Filtering]","fwp.fwpmengineclose0_func","fwpmu/FwpmEngineClose0"]
old-location: fwp\fwpmengineclose0_func.htm
tech.root: fwp
ms.assetid: e96165a8-95ad-4cb0-9f45-e8af22f83a52
ms.date: 12/05/2018
ms.keywords: FwpmEngineClose0, FwpmEngineClose0 function [Filtering], fwp.fwpmengineclose0_func, fwpmu/FwpmEngineClose0
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
 - FwpmEngineClose0
 - fwpmu/FwpmEngineClose0
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
 - FwpmEngineClose0
---

# FwpmEngineClose0 function


## -description

The <b>FwpmEngineClose0</b> function closes a session to a filter engine.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

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
The session was closed successfully.

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

After an application has completed adding or removing system objects, it may call the <b>FwpmEngineClose0</b> function to close the open session to the filter engine.

A filter engine session is also closed when a client process terminates.

If this function is called with a transaction in progress, the transaction will be aborted.

<b>FwpmEngineClose0</b> is a specific implementation of FwpmEngineClose. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a>



[Kernel-Mode FwpmEngineClose0](nf-fwpmu-fwpmengineclose0.md)