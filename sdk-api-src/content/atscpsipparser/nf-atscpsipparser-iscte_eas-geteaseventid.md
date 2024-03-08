---
UID: NF:atscpsipparser.ISCTE_EAS.GetEASEventID
title: ISCTE_EAS::GetEASEventID (atscpsipparser.h)
description: The GetEASEventID method returns the identifier of this emergency event.
helpviewer_keywords: ["GetEASEventID","GetEASEventID method [Microsoft TV Technologies]","GetEASEventID method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetEASEventID method","ISCTE_EAS.GetEASEventID","ISCTE_EAS::GetEASEventID","ISCTE_EASGetEASEventID","atscpsipparser/ISCTE_EAS::GetEASEventID","mstv.iscte_eas_geteaseventid"]
old-location: mstv\iscte_eas_geteaseventid.htm
tech.root: mstv
ms.assetid: d501fa7c-c1a8-42bc-af71-a966a7cba9f6
ms.date: 12/05/2018
ms.keywords: GetEASEventID, GetEASEventID method [Microsoft TV Technologies], GetEASEventID method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetEASEventID method, ISCTE_EAS.GetEASEventID, ISCTE_EAS::GetEASEventID, ISCTE_EASGetEASEventID, atscpsipparser/ISCTE_EAS::GetEASEventID, mstv.iscte_eas_geteaseventid
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
 - ISCTE_EAS::GetEASEventID
 - atscpsipparser/ISCTE_EAS::GetEASEventID
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
 - ISCTE_EAS.GetEASEventID
---

# ISCTE_EAS::GetEASEventID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetEASEventID</b> method returns the identifier of this emergency event.

## -parameters

### -param pwVal [out]

Receives the EAS_Event_ID field.

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