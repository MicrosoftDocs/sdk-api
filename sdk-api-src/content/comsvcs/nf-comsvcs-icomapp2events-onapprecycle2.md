---
UID: NF:comsvcs.IComApp2Events.OnAppRecycle2
title: IComApp2Events::OnAppRecycle2 (comsvcs.h)
description: Generated when the server application process is marked for recycling termination.
helpviewer_keywords: ["CRR_ACTIVATION_LIMIT","CRR_CALL_LIMIT","CRR_LIFETIME_LIMIT","CRR_MEMORY_LIMIT","CRR_NO_REASON_SUPPLIED","CRR_RECYCLED_FROM_UI","IComApp2Events interface [COM+]","OnAppRecycle2 method","IComApp2Events.OnAppRecycle2","IComApp2Events::OnAppRecycle2","OnAppRecycle2","OnAppRecycle2 method [COM+]","OnAppRecycle2 method [COM+]","IComApp2Events interface","_dtc_IComApp2Events_OnAppRecycle2","comsvcs/IComApp2Events::OnAppRecycle2","cos.icomapp2events_onapprecycle2"]
old-location: cos\icomapp2events_onapprecycle2.htm
tech.root: cos
ms.assetid: 36be1f17-05cc-4c0a-97aa-84abd46de801
ms.date: 12/05/2018
ms.keywords: CRR_ACTIVATION_LIMIT, CRR_CALL_LIMIT, CRR_LIFETIME_LIMIT, CRR_MEMORY_LIMIT, CRR_NO_REASON_SUPPLIED, CRR_RECYCLED_FROM_UI, IComApp2Events interface [COM+],OnAppRecycle2 method, IComApp2Events.OnAppRecycle2, IComApp2Events::OnAppRecycle2, OnAppRecycle2, OnAppRecycle2 method [COM+], OnAppRecycle2 method [COM+],IComApp2Events interface, _dtc_IComApp2Events_OnAppRecycle2, comsvcs/IComApp2Events::OnAppRecycle2, cos.icomapp2events_onapprecycle2
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComApp2Events::OnAppRecycle2
 - comsvcs/IComApp2Events::OnAppRecycle2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComApp2Events.OnAppRecycle2
---

# IComApp2Events::OnAppRecycle2


## -description

Generated when the server application process is marked for recycling termination.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidApp [in]

The application ID.

### -param guidProcess [in]

The process ID.

### -param lReason [in]

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

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomapp2events">IComApp2Events</a>