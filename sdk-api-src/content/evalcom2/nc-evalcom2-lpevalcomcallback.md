---
UID: NC:evalcom2.LPEVALCOMCALLBACK
title: LPEVALCOMCALLBACK (evalcom2.h)
description: The LPEVALCOMCALLBACK specification defines a callback function prototype. The IValidate::SetStatus method enables an authoring tool to receive information about the progress of validation through the registered callback function.
helpviewer_keywords: ["LPEVALCOMCALLBACK","LPEVALCOMCALLBACK callback","LPEVALCOMCALLBACK callback function","evalcom2/LPEVALCOMCALLBACK","ieStatusCancel","ieStatusCreateEngine","ieStatusFail","ieStatusICECount","ieStatusMerge","ieStatusRunICE","ieStatusShutdown","ieStatusStarting","ieStatusSuccess","ieStatusSummaryInfo","setup.lpevalcomcallback"]
old-location: setup\lpevalcomcallback.htm
tech.root: setup
ms.assetid: 76504031-b63a-40fc-aa5b-728f3551057b
ms.date: 12/05/2018
ms.keywords: LPEVALCOMCALLBACK, LPEVALCOMCALLBACK callback, LPEVALCOMCALLBACK callback function, evalcom2/LPEVALCOMCALLBACK, ieStatusCancel, ieStatusCreateEngine, ieStatusFail, ieStatusICECount, ieStatusMerge, ieStatusRunICE, ieStatusShutdown, ieStatusStarting, ieStatusSuccess, ieStatusSummaryInfo, setup.lpevalcomcallback
req.header: evalcom2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Evalcom2.dll version 3.0.3790.371 or later
req.target-min-winversvr: 
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
 - LPEVALCOMCALLBACK
 - evalcom2/LPEVALCOMCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - evalcom2.h
api_name:
 - LPEVALCOMCALLBACK
---

## -description

The <b>LPEVALCOMCALLBACK</b> specification defines a callback function prototype. The <a href="/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus">IValidate::SetStatus</a> method enables an authoring tool to receive information about the progress of validation through the registered callback function.

## -parameters

### -param iStatus [in]

Specifies the status message sent by evalcom2. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
The value of this param

</td>
</tr>
<tr>
<td width="40%"><a id="ieStatusICECount"></a><a id="iestatusicecount"></a><a id="IESTATUSICECOUNT"></a><dl>
<dt><b>ieStatusICECount</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Number of ICEs that are being run.

</td>
</tr>
<tr>
<td width="40%"><a id="ieStatusMerge"></a><a id="iestatusmerge"></a><a id="IESTATUSMERGE"></a><dl>
<dt><b>ieStatusMerge</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Merging the package or merge module with the .cub file.

</td>
</tr>
<tr>
<td width="40%"><a id="ieStatusSummaryInfo"></a><a id="iestatussummaryinfo"></a><a id="IESTATUSSUMMARYINFO"></a><dl>
<dt><b>ieStatusSummaryInfo</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Merging summary information streams.

</td>
</tr>
<tr>
<td width="40%"><a id="ieStatusCreateEngine"></a><a id="iestatuscreateengine"></a><a id="IESTATUSCREATEENGINE"></a><dl>
<dt><b>ieStatusCreateEngine</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Preparing to run the ICEs.

</td>
</tr>
<tr>
<td width="40%"><a id="ieStatusRunICE"></a><a id="iestatusrunice"></a><a id="IESTATUSRUNICE"></a><dl>
<dt><b>ieStatusRunICE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Running an individual ICE.

</td>
</tr>
<tr>
<td width="40%"><a id="ieStatusStarting"></a><a id="iestatusstarting"></a><a id="IESTATUSSTARTING"></a><dl>
<dt><b>ieStatusStarting</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Starting validation.

</td>
</tr>
<tr>
<td width="40%"><a id="ieStatusShutdown"></a><a id="iestatusshutdown"></a><a id="IESTATUSSHUTDOWN"></a><dl>
<dt><b>ieStatusShutdown</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Finish running the ICEs.

</td>
</tr>
<tr>
<td width="40%"><a id="ieStatusSuccess"></a><a id="iestatussuccess"></a><a id="IESTATUSSUCCESS"></a><dl>
<dt><b>ieStatusSuccess</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Validation completed successfully.

</td>
</tr>
<tr>
<td width="40%"><a id="ieStatusFail"></a><a id="iestatusfail"></a><a id="IESTATUSFAIL"></a><dl>
<dt><b>ieStatusFail</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Validation failed. 

</td>
</tr>
<tr>
<td width="40%"><a id="ieStatusCancel"></a><a id="iestatuscancel"></a><a id="IESTATUSCANCEL"></a><dl>
<dt><b>ieStatusCancel</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Validation was canceled.

</td>
</tr>
</table>

### -param szData

A string value containing information appropriate to the status. The value of <i>szwData</i> should be the number of ICEs that are being run if <i>iStatus</i> is <b>ieStatusICECount</b>. The value of <i>szwData</i> should be the name of the ICE being run if <i>iStatus</i> is <b>ieStatusRunICE</b>. Otherwise, the value of <i>szwData</i> should be <b>NULL</b>. The callback function should accept <b>NULL</b> as a possible value for this parameter.

### -param pContext

Pointer to an application context passed to the <a href="/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus">SetStatus</a> method. This parameter can be used for error checking.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Validation procedure should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Validation was canceled. The callback function return <b>FALSE</b> to stop validation.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus">SetStatus</a> method and <b>LPEVALCOMCALLBACK</b> can be used to provide progress information.  For example, the <b>ieStatusICECount</b> message can provide the overall tick count for a progress bar.  For each <b>ieStatusRunICE</b> message received, the caller can increment the progress bar one tick.

## -see-also

<a href="/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate">IValidate</a>



<a href="/windows/desktop/Msi/using-evalcom2">Using Evalcom2</a>



<a href="/windows/desktop/Msi/validation-callback-functions">Validation Callback Functions</a>