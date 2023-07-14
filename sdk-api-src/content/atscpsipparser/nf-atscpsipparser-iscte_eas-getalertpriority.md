---
UID: NF:atscpsipparser.ISCTE_EAS.GetAlertPriority
title: ISCTE_EAS::GetAlertPriority (atscpsipparser.h)
description: The GetAlertPriority method returns the alert priority.
helpviewer_keywords: ["GetAlertPriority","GetAlertPriority method [Microsoft TV Technologies]","GetAlertPriority method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetAlertPriority method","ISCTE_EAS.GetAlertPriority","ISCTE_EAS::GetAlertPriority","ISCTE_EASGetAlertPriority","atscpsipparser/ISCTE_EAS::GetAlertPriority","mstv.iscte_eas_getalertpriority"]
old-location: mstv\iscte_eas_getalertpriority.htm
tech.root: mstv
ms.assetid: 3862ae19-972b-4822-8b52-5a868a2fc58d
ms.date: 12/05/2018
ms.keywords: GetAlertPriority, GetAlertPriority method [Microsoft TV Technologies], GetAlertPriority method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetAlertPriority method, ISCTE_EAS.GetAlertPriority, ISCTE_EAS::GetAlertPriority, ISCTE_EASGetAlertPriority, atscpsipparser/ISCTE_EAS::GetAlertPriority, mstv.iscte_eas_getalertpriority
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - ISCTE_EAS::GetAlertPriority
 - atscpsipparser/ISCTE_EAS::GetAlertPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - ISCTE_EAS.GetAlertPriority
---

# ISCTE_EAS::GetAlertPriority


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetAlertPriority</b> method returns the alert priority.

## -parameters

### -param pbVal [out]

Receives the alert_priority field.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-initialize">ISCTE_EAS::Initialize</a> method was not called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS Interface</a>