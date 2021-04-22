---
UID: NF:wdspxe.PxeTrace
title: PxeTrace function (wdspxe.h)
description: Adds a trace entry to the PXE log.
helpviewer_keywords: ["PXE_TRACE_ERROR","PXE_TRACE_FATAL","PXE_TRACE_INFO","PXE_TRACE_VERBOSE","PXE_TRACE_WARNING","PxeTrace","PxeTrace function [Windows Deployment Services]","wds.pxetrace","wdspxe/PxeTrace"]
old-location: wds\pxetrace.htm
tech.root: wds
ms.assetid: 220f15bf-f33a-4706-a52d-f11c40f49ac0
ms.date: 12/05/2018
ms.keywords: PXE_TRACE_ERROR, PXE_TRACE_FATAL, PXE_TRACE_INFO, PXE_TRACE_VERBOSE, PXE_TRACE_WARNING, PxeTrace, PxeTrace function [Windows Deployment Services], wds.pxetrace, wdspxe/PxeTrace
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PxeTrace
 - wdspxe/PxeTrace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeTrace
---

# PxeTrace function


## -description

Adds a trace entry to the PXE log.

## -parameters

### -param hProvider [in]

<b>HANDLE</b> passed to the 
      <a href="/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a> function.

### -param Severity [in]

Severity of trace entry.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_TRACE_VERBOSE"></a><a id="pxe_trace_verbose"></a><dl>
<dt><b>PXE_TRACE_VERBOSE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The trace entry is verbose and would primarily be useful when debugging.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_TRACE_INFO"></a><a id="pxe_trace_info"></a><dl>
<dt><b>PXE_TRACE_INFO</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The trace entry is informational, but does not indicate a warning condition.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_TRACE_WARNING"></a><a id="pxe_trace_warning"></a><dl>
<dt><b>PXE_TRACE_WARNING</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The trace message indicates a warning.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_TRACE_ERROR"></a><a id="pxe_trace_error"></a><dl>
<dt><b>PXE_TRACE_ERROR</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
The trace message indicates an error condition.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_TRACE_FATAL"></a><a id="pxe_trace_fatal"></a><dl>
<dt><b>PXE_TRACE_FATAL</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The trace message indicates a fatal error condition.

</td>
</tr>
</table>

### -param pszFormat [in]

Address of a buffer that contains a printf-style format string.

### -param ...

Optional arguments. The number and type of argument parameters depend on the format control string pointed 
      to by the <i>pszFormat</i> parameter.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>

