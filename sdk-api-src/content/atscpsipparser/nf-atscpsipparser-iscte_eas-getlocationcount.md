---
UID: NF:atscpsipparser.ISCTE_EAS.GetLocationCount
title: ISCTE_EAS::GetLocationCount (atscpsipparser.h)
description: The GetLocationCount method returns the number of locations in the EAS table.
helpviewer_keywords: ["GetLocationCount","GetLocationCount method [Microsoft TV Technologies]","GetLocationCount method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetLocationCount method","ISCTE_EAS.GetLocationCount","ISCTE_EAS::GetLocationCount","ISCTE_EASGetLocationCount","atscpsipparser/ISCTE_EAS::GetLocationCount","mstv.iscte_eas_getlocationcount"]
old-location: mstv\iscte_eas_getlocationcount.htm
tech.root: mstv
ms.assetid: f498ead0-246d-4741-a995-45a5cf63847e
ms.date: 12/05/2018
ms.keywords: GetLocationCount, GetLocationCount method [Microsoft TV Technologies], GetLocationCount method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetLocationCount method, ISCTE_EAS.GetLocationCount, ISCTE_EAS::GetLocationCount, ISCTE_EASGetLocationCount, atscpsipparser/ISCTE_EAS::GetLocationCount, mstv.iscte_eas_getlocationcount
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
 - ISCTE_EAS::GetLocationCount
 - atscpsipparser/ISCTE_EAS::GetLocationCount
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
 - ISCTE_EAS.GetLocationCount
---

# ISCTE_EAS::GetLocationCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetLocationCount</b> method returns the number of locations in the EAS table.

## -parameters

### -param pbVal [out]

Receives the location_code_count field.

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