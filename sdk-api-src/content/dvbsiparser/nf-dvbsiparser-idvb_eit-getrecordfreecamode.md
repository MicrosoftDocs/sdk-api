---
UID: NF:dvbsiparser.IDVB_EIT.GetRecordFreeCAMode
title: IDVB_EIT::GetRecordFreeCAMode (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordFreeCAMode","GetRecordFreeCAMode method [Microsoft TV Technologies]","GetRecordFreeCAMode method [Microsoft TV Technologies]","IDVB_EIT interface","IDVB_EIT interface [Microsoft TV Technologies]","GetRecordFreeCAMode method","IDVB_EIT.GetRecordFreeCAMode","IDVB_EIT::GetRecordFreeCAMode","IDVB_EITGetRecordFreeCAMode","dvbsiparser/IDVB_EIT::GetRecordFreeCAMode","mstv.idvb_eit_getrecordfreecamode"]
old-location: mstv\idvb_eit_getrecordfreecamode.htm
tech.root: mstv
ms.assetid: d154772c-3e7c-49f8-90d1-4ff1be01e4d0
ms.date: 12/05/2018
ms.keywords: GetRecordFreeCAMode, GetRecordFreeCAMode method [Microsoft TV Technologies], GetRecordFreeCAMode method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetRecordFreeCAMode method, IDVB_EIT.GetRecordFreeCAMode, IDVB_EIT::GetRecordFreeCAMode, IDVB_EITGetRecordFreeCAMode, dvbsiparser/IDVB_EIT::GetRecordFreeCAMode, mstv.idvb_eit_getrecordfreecamode
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
 - IDVB_EIT::GetRecordFreeCAMode
 - dvbsiparser/IDVB_EIT::GetRecordFreeCAMode
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
 - IDVB_EIT.GetRecordFreeCAMode
---

# IDVB_EIT::GetRecordFreeCAMode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordFreeCAMode</b> method queries whether any of the component streams for an event are scrambled.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number for the event, indexed from zero. Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getcountofrecords">IDVB_EIT::GetCountOfRecords</a> to get the number of records in the EIT.

### -param pfVal [out]

Pointer to a variable that receives a Boolean value. The value is <b>TRUE</b> if the free_CA_mode bit is set, which indicates that one or more streams are scrambled. Otherwise, the value is <b>FALSE</b>.

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
<b>NULL</b> pointer argument.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT Interface</a>