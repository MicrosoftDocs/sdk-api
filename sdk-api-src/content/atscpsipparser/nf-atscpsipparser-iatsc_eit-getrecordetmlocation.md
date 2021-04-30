---
UID: NF:atscpsipparser.IATSC_EIT.GetRecordEtmLocation
title: IATSC_EIT::GetRecordEtmLocation (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordEtmLocation","GetRecordEtmLocation method [Microsoft TV Technologies]","GetRecordEtmLocation method [Microsoft TV Technologies]","IATSC_EIT interface","IATSC_EIT interface [Microsoft TV Technologies]","GetRecordEtmLocation method","IATSC_EIT.GetRecordEtmLocation","IATSC_EIT::GetRecordEtmLocation","IATSC_EITGetRecordEtmLocation","atscpsipparser/IATSC_EIT::GetRecordEtmLocation","mstv.iatsc_eit_getrecordetmlocation"]
old-location: mstv\iatsc_eit_getrecordetmlocation.htm
tech.root: mstv
ms.assetid: 4997f1dc-64b2-4739-90f5-5642a2d71958
ms.date: 12/05/2018
ms.keywords: GetRecordEtmLocation, GetRecordEtmLocation method [Microsoft TV Technologies], GetRecordEtmLocation method [Microsoft TV Technologies],IATSC_EIT interface, IATSC_EIT interface [Microsoft TV Technologies],GetRecordEtmLocation method, IATSC_EIT.GetRecordEtmLocation, IATSC_EIT::GetRecordEtmLocation, IATSC_EITGetRecordEtmLocation, atscpsipparser/IATSC_EIT::GetRecordEtmLocation, mstv.iatsc_eit_getrecordetmlocation
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
 - IATSC_EIT::GetRecordEtmLocation
 - atscpsipparser/IATSC_EIT::GetRecordEtmLocation
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
 - IATSC_EIT.GetRecordEtmLocation
---

# IATSC_EIT::GetRecordEtmLocation


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordEtmLocation</b> method returns the extended text message (ETM) location for a record in the EIT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getcountofrecords">IATSC_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.

### -param pbVal [out]

Receives the ETM_location field.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of bounds.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_eit">IATSC_EIT Interface</a>