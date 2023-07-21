---
UID: NF:atscpsipparser.ISCTE_EAS.GetSequencyNumber
title: ISCTE_EAS::GetSequencyNumber (atscpsipparser.h)
description: The GetSequencyNumbermethod returns the sequence number.
helpviewer_keywords: ["GetSequencyNumber","GetSequencyNumber method [Microsoft TV Technologies]","GetSequencyNumber method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetSequencyNumber method","ISCTE_EAS.GetSequencyNumber","ISCTE_EAS::GetSequencyNumber","ISCTE_EASGetSequencyNumber","atscpsipparser/ISCTE_EAS::GetSequencyNumber","mstv.iscte_eas_getsequencynumber"]
old-location: mstv\iscte_eas_getsequencynumber.htm
tech.root: mstv
ms.assetid: c7988bb1-0c89-4f6f-beda-cbfd04a9b128
ms.date: 12/05/2018
ms.keywords: GetSequencyNumber, GetSequencyNumber method [Microsoft TV Technologies], GetSequencyNumber method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetSequencyNumber method, ISCTE_EAS.GetSequencyNumber, ISCTE_EAS::GetSequencyNumber, ISCTE_EASGetSequencyNumber, atscpsipparser/ISCTE_EAS::GetSequencyNumber, mstv.iscte_eas_getsequencynumber
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
 - ISCTE_EAS::GetSequencyNumber
 - atscpsipparser/ISCTE_EAS::GetSequencyNumber
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
 - ISCTE_EAS.GetSequencyNumber
---

# ISCTE_EAS::GetSequencyNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetSequencyNumber</b> method returns the sequence number.

## -parameters

### -param pbVal [out]

Receives the sequence_number field.

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