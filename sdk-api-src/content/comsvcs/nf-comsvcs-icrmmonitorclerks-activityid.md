---
UID: NF:comsvcs.ICrmMonitorClerks.ActivityId
title: ICrmMonitorClerks::ActivityId (comsvcs.h)
description: Retrieves the activity ID of the CRM Worker for the specified index.
helpviewer_keywords: ["ActivityId","ActivityId method [COM+]","ActivityId method [COM+]","ICrmMonitorClerks interface","ICrmMonitorClerks interface [COM+]","ActivityId method","ICrmMonitorClerks.ActivityId","ICrmMonitorClerks::ActivityId","_dtc_ICrmMonitorClerks_ActivityId","comsvcs/ICrmMonitorClerks::ActivityId","cos.icrmmonitorclerks_activityid"]
old-location: cos\icrmmonitorclerks_activityid.htm
tech.root: cos
ms.assetid: 19a242a6-ce21-4ce5-984e-cc2220476e2b
ms.date: 12/05/2018
ms.keywords: ActivityId, ActivityId method [COM+], ActivityId method [COM+],ICrmMonitorClerks interface, ICrmMonitorClerks interface [COM+],ActivityId method, ICrmMonitorClerks.ActivityId, ICrmMonitorClerks::ActivityId, _dtc_ICrmMonitorClerks_ActivityId, comsvcs/ICrmMonitorClerks::ActivityId, cos.icrmmonitorclerks_activityid
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICrmMonitorClerks::ActivityId
 - comsvcs/ICrmMonitorClerks::ActivityId
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
 - ICrmMonitorClerks.ActivityId
---

# ICrmMonitorClerks::ActivityId


## -description

Retrieves the activity ID of the CRM Worker for the specified index.

## -parameters

### -param Index [in]

The index of the required CRM clerk as a numeric <b>Variant</b>, or the instance CLSID as a <b>Variant</b> string.

### -param pItem [out]

The activity ID of the CRM Worker.

## -returns

This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is incorrect.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitorclerks">ICrmMonitorClerks</a>