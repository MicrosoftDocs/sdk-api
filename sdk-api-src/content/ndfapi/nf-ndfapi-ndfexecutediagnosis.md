---
UID: NF:ndfapi.NdfExecuteDiagnosis
title: NdfExecuteDiagnosis function (ndfapi.h)
description: The NdfExecuteDiagnosis function is used to diagnose the root cause of the incident that has occurred.
helpviewer_keywords: ["NdfExecuteDiagnosis","NdfExecuteDiagnosis function [NDF]","ndf.ndfexecutediagnosis","ndfapi/NdfExecuteDiagnosis"]
old-location: ndf\ndfexecutediagnosis.htm
tech.root: NDF
ms.assetid: b65f30c3-53d5-4282-8d38-5723772f15fc
ms.date: 12/05/2018
ms.keywords: NdfExecuteDiagnosis, NdfExecuteDiagnosis function [NDF], ndf.ndfexecutediagnosis, ndfapi/NdfExecuteDiagnosis
req.header: ndfapi.h
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
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NdfExecuteDiagnosis
 - ndfapi/NdfExecuteDiagnosis
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-net-nfdapi-l1-1-1.dll
 - ext-ms-win-net-nfdapi-l1-1-0.dll
 - Ndfapi.dll
api_name:
 - NdfExecuteDiagnosis
---

# NdfExecuteDiagnosis function


## -description

The <b>NdfExecuteDiagnosis</b> function is used to diagnose the root cause of the incident that has occurred.

## -parameters

### -param handle

Type: <b>NDFHANDLE</b>

Handle to the Network Diagnostics Framework incident.

### -param hwnd

Type: <b>HWND</b>

Handle to the window that is intended to display the diagnostic information. If specified, the NDF UI is modal to the window.  If <b>NULL</b>, the UI is non-modal.

## -returns

Type: <b>HRESULT</b>

Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>handle</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcloseincident">NdfCloseIncident</a>



<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcreateincident">NdfCreateIncident</a>



<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcreatewinsockincident">NdfCreateWinSockIncident</a>