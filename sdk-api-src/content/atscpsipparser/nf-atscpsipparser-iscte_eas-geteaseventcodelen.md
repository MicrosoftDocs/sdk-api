---
UID: NF:atscpsipparser.ISCTE_EAS.GetEASEventCodeLen
title: ISCTE_EAS::GetEASEventCodeLen (atscpsipparser.h)
description: The GetEASEventCodeLen method returns the size of the EAS event code.
helpviewer_keywords: ["GetEASEventCodeLen","GetEASEventCodeLen method [Microsoft TV Technologies]","GetEASEventCodeLen method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetEASEventCodeLen method","ISCTE_EAS.GetEASEventCodeLen","ISCTE_EAS::GetEASEventCodeLen","ISCTE_EASGetEASEventCodeLen","atscpsipparser/ISCTE_EAS::GetEASEventCodeLen","mstv.iscte_eas_geteaseventcodelen"]
old-location: mstv\iscte_eas_geteaseventcodelen.htm
tech.root: mstv
ms.assetid: d6e05cd0-d043-4f15-b25b-28402035943b
ms.date: 12/05/2018
ms.keywords: GetEASEventCodeLen, GetEASEventCodeLen method [Microsoft TV Technologies], GetEASEventCodeLen method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetEASEventCodeLen method, ISCTE_EAS.GetEASEventCodeLen, ISCTE_EAS::GetEASEventCodeLen, ISCTE_EASGetEASEventCodeLen, atscpsipparser/ISCTE_EAS::GetEASEventCodeLen, mstv.iscte_eas_geteaseventcodelen
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
 - ISCTE_EAS::GetEASEventCodeLen
 - atscpsipparser/ISCTE_EAS::GetEASEventCodeLen
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
 - ISCTE_EAS.GetEASEventCodeLen
---

# ISCTE_EAS::GetEASEventCodeLen


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetEASEventCodeLen</b> method returns the size of the EAS event code.

## -parameters

### -param pbVal [out]

Receives the size of the EAS event code, in bytes. To get the event code, allocate a buffer of this size and call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-geteaseventcode">ISCTE_EAS::GetEASEventCode</a>.

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