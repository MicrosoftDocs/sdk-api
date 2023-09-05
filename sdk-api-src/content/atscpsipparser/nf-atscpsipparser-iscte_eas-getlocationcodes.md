---
UID: NF:atscpsipparser.ISCTE_EAS.GetLocationCodes
title: ISCTE_EAS::GetLocationCodes (atscpsipparser.h)
description: The GetLocationCodes method returns location codes from the EAS table.
helpviewer_keywords: ["GetLocationCodes","GetLocationCodes method [Microsoft TV Technologies]","GetLocationCodes method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetLocationCodes method","ISCTE_EAS.GetLocationCodes","ISCTE_EAS::GetLocationCodes","ISCTE_EASGetLocationCodes","atscpsipparser/ISCTE_EAS::GetLocationCodes","mstv.iscte_eas_getlocationcodes"]
old-location: mstv\iscte_eas_getlocationcodes.htm
tech.root: mstv
ms.assetid: 31fa68d4-1719-4a93-bec9-6a7ba4f36c0b
ms.date: 12/05/2018
ms.keywords: GetLocationCodes, GetLocationCodes method [Microsoft TV Technologies], GetLocationCodes method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetLocationCodes method, ISCTE_EAS.GetLocationCodes, ISCTE_EAS::GetLocationCodes, ISCTE_EASGetLocationCodes, atscpsipparser/ISCTE_EAS::GetLocationCodes, mstv.iscte_eas_getlocationcodes
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
 - ISCTE_EAS::GetLocationCodes
 - atscpsipparser/ISCTE_EAS::GetLocationCodes
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
 - ISCTE_EAS.GetLocationCodes
---

# ISCTE_EAS::GetLocationCodes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetLocationCodes</b> method returns location codes from the EAS table.

## -parameters

### -param bIndex [in]

The zero-based index of the location codes to retrieve. Call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getlocationcount">ISCTE_EAS::GetLocationCount</a> to get the number of locations.

### -param pbState [out]

Receives the state_code field.

### -param pbCountySubdivision [out]

Receives the county_subdivision field.

### -param pwCounty [out]

Receives the county_code field.

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
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
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