---
UID: NF:dvbsiparser.IDVB_SIT.GetCountOfRecords
title: IDVB_SIT::GetCountOfRecords (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IDVB_SIT interface","IDVB_SIT interface [Microsoft TV Technologies]","GetCountOfRecords method","IDVB_SIT.GetCountOfRecords","IDVB_SIT::GetCountOfRecords","IDVB_SITGetCountOfRecords","dvbsiparser/IDVB_SIT::GetCountOfRecords","mstv.idvb_sit_getcountofrecords"]
old-location: mstv\idvb_sit_getcountofrecords.htm
tech.root: mstv
ms.assetid: 93d04770-9ec5-411c-8892-4b9a7944d681
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDVB_SIT interface, IDVB_SIT interface [Microsoft TV Technologies],GetCountOfRecords method, IDVB_SIT.GetCountOfRecords, IDVB_SIT::GetCountOfRecords, IDVB_SITGetCountOfRecords, dvbsiparser/IDVB_SIT::GetCountOfRecords, mstv.idvb_sit_getcountofrecords
req.header: dvbsiparser.h
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
 - IDVB_SIT::GetCountOfRecords
 - dvbsiparser/IDVB_SIT::GetCountOfRecords
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_SIT.GetCountOfRecords
---

# IDVB_SIT::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfRecords</b> method returns the number of records in the SIT.

## -parameters

### -param pdwVal [out]

Pointer to a variable that receives the number of records.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sit">IDVB_SIT Interface</a>