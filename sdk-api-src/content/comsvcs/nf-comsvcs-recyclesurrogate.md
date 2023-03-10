---
UID: NF:comsvcs.RecycleSurrogate
title: RecycleSurrogate function (comsvcs.h)
description: Recycles the calling process.
helpviewer_keywords: ["CRR_ACTIVATION_LIMIT","CRR_CALL_LIMIT","CRR_LIFETIME_LIMIT","CRR_MEMORY_LIMIT","CRR_NO_REASON_SUPPLIED","CRR_RECYCLED_FROM_UI","RecycleSurrogate","RecycleSurrogate function [COM+]","_cos_recyclesurrogate","comsvcs/RecycleSurrogate","cos.recyclesurrogate"]
old-location: cos\recyclesurrogate.htm
tech.root: cos
ms.assetid: d75f5894-f711-48f8-a6f5-be7ac594dc42
ms.date: 12/05/2018
ms.keywords: CRR_ACTIVATION_LIMIT, CRR_CALL_LIMIT, CRR_LIFETIME_LIMIT, CRR_MEMORY_LIMIT, CRR_NO_REASON_SUPPLIED, CRR_RECYCLED_FROM_UI, RecycleSurrogate, RecycleSurrogate function [COM+], _cos_recyclesurrogate, comsvcs/RecycleSurrogate, cos.recyclesurrogate
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ComSvcs.lib
req.dll: ComSvcs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RecycleSurrogate
 - comsvcs/RecycleSurrogate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComSvcs.dll
api_name:
 - RecycleSurrogate
---

# RecycleSurrogate function


## -description

Recycles the calling process.

For similar functionality, see <a href="/previous-versions/windows/desktop/legacy/ms679243(v=vs.85)">IMTxAS::RecycleSurrogate</a>.

## -parameters

### -param lReasonCode [in]

The reason code that explains why a process was recycled. The following codes are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRR_NO_REASON_SUPPLIED"></a><a id="crr_no_reason_supplied"></a><dl>
<dt><b>CRR_NO_REASON_SUPPLIED</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The reason is not specified.

</td>
</tr>
<tr>
<td width="40%"><a id="CRR_LIFETIME_LIMIT"></a><a id="crr_lifetime_limit"></a><dl>
<dt><b>CRR_LIFETIME_LIMIT</b></dt>
<dt>xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
The specified number of minutes that an application runs before recycling was reached.

</td>
</tr>
<tr>
<td width="40%"><a id="CRR_ACTIVATION_LIMIT"></a><a id="crr_activation_limit"></a><dl>
<dt><b>CRR_ACTIVATION_LIMIT</b></dt>
<dt>0xFFFFFFFE</dt>
</dl>
</td>
<td width="60%">
The specified number of activations was reached.

</td>
</tr>
<tr>
<td width="40%"><a id="CRR_CALL_LIMIT"></a><a id="crr_call_limit"></a><dl>
<dt><b>CRR_CALL_LIMIT</b></dt>
<dt>0xFFFFFFFD</dt>
</dl>
</td>
<td width="60%">
The specified number of calls to configured objects in the application was reached.

</td>
</tr>
<tr>
<td width="40%"><a id="CRR_MEMORY_LIMIT"></a><a id="crr_memory_limit"></a><dl>
<dt><b>CRR_MEMORY_LIMIT</b></dt>
<dt>0xFFFFFFFC</dt>
</dl>
</td>
<td width="60%">
The specified memory usage that a process cannot exceed was reached.

</td>
</tr>
<tr>
<td width="40%"><a id="CRR_RECYCLED_FROM_UI"></a><a id="crr_recycled_from_ui"></a><dl>
<dt><b>CRR_RECYCLED_FROM_UI</b></dt>
<dt>xFFFFFFFB</dt>
</dl>
</td>
<td width="60%">
An administrator decided to recycle the process through the Component Services administration tool.

</td>
</tr>
</table>

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-recycleapplicationinstances">ICOMAdminCatalog2::RecycleApplicationInstances</a>