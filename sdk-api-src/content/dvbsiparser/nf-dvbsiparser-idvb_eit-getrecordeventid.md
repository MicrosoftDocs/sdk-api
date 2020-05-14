---
UID: NF:dvbsiparser.IDVB_EIT.GetRecordEventId
title: IDVB_EIT::GetRecordEventId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.helpviewer_keywords: ["GetRecordEventId","GetRecordEventId method [Microsoft TV Technologies]","GetRecordEventId method [Microsoft TV Technologies]","IDVB_EIT interface","IDVB_EIT interface [Microsoft TV Technologies]","GetRecordEventId method","IDVB_EIT.GetRecordEventId","IDVB_EIT::GetRecordEventId","IDVB_EITGetRecordEventId","dvbsiparser/IDVB_EIT::GetRecordEventId","mstv.idvb_eit_getrecordeventid"]
old-location: mstv\idvb_eit_getrecordeventid.htm
tech.root: mstv
ms.assetid: cfdaea8c-bcc9-4689-94b9-a651fdc06484
ms.date: 12/05/2018
ms.keywords: GetRecordEventId, GetRecordEventId method [Microsoft TV Technologies], GetRecordEventId method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetRecordEventId method, IDVB_EIT.GetRecordEventId, IDVB_EIT::GetRecordEventId, IDVB_EITGetRecordEventId, dvbsiparser/IDVB_EIT::GetRecordEventId, mstv.idvb_eit_getrecordeventid
f1_keywords:
- dvbsiparser/IDVB_EIT.GetRecordEventId
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IDVB_EIT.GetRecordEventId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_EIT::GetRecordEventId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordEventId</b> method returns the event identifier for a record in the EIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getcountofrecords">IDVB_EIT::GetCountOfRecords</a> to get the number of records in the EIT.


### -param pwVal [out]

Pointer to a variable that receives the event_id field.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT Interface</a>
 

 

