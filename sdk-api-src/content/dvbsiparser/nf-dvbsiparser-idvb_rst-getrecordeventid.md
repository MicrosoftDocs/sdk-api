---
UID: NF:dvbsiparser.IDVB_RST.GetRecordEventId
title: IDVB_RST::GetRecordEventId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.helpviewer_keywords: ["GetRecordEventId","GetRecordEventId method [Microsoft TV Technologies]","GetRecordEventId method [Microsoft TV Technologies]","IDVB_RST interface","IDVB_RST interface [Microsoft TV Technologies]","GetRecordEventId method","IDVB_RST.GetRecordEventId","IDVB_RST::GetRecordEventId","IDVB_RSTGetRecordEventId","dvbsiparser/IDVB_RST::GetRecordEventId","mstv.idvb_rst_getrecordeventid"]
old-location: mstv\idvb_rst_getrecordeventid.htm
tech.root: mstv
ms.assetid: 4263160a-dd00-42a8-9ed3-6b266c0d6355
ms.date: 12/05/2018
ms.keywords: GetRecordEventId, GetRecordEventId method [Microsoft TV Technologies], GetRecordEventId method [Microsoft TV Technologies],IDVB_RST interface, IDVB_RST interface [Microsoft TV Technologies],GetRecordEventId method, IDVB_RST.GetRecordEventId, IDVB_RST::GetRecordEventId, IDVB_RSTGetRecordEventId, dvbsiparser/IDVB_RST::GetRecordEventId, mstv.idvb_rst_getrecordeventid
f1_keywords:
- dvbsiparser/IDVB_RST.GetRecordEventId
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
- IDVB_RST.GetRecordEventId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_RST::GetRecordEventId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordEventId</b> method returns the event identifier for a record in the RST.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getcountofrecords">IDVB_RST::GetCountOfRecords</a> method to get the number of records in the RST.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_rst">IDVB_RST Interface</a>
 

 

