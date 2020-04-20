---
UID: NF:dvbsiparser.IDVB_SDT.GetCountOfRecords
title: IDVB_SDT::GetCountOfRecords (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IDVB_SDT interface","IDVB_SDT interface [Microsoft TV Technologies]","GetCountOfRecords method","IDVB_SDT.GetCountOfRecords","IDVB_SDT::GetCountOfRecords","IDVB_SDTGetCountOfRecords","dvbsiparser/IDVB_SDT::GetCountOfRecords","mstv.idvb_sdt_getcountofrecords"]
old-location: mstv\idvb_sdt_getcountofrecords.htm
tech.root: mstv
ms.assetid: 9815ba89-d5c2-4d13-8ed1-478953836bc7
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetCountOfRecords method, IDVB_SDT.GetCountOfRecords, IDVB_SDT::GetCountOfRecords, IDVB_SDTGetCountOfRecords, dvbsiparser/IDVB_SDT::GetCountOfRecords, mstv.idvb_sdt_getcountofrecords
f1_keywords:
- dvbsiparser/IDVB_SDT.GetCountOfRecords
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
- IDVB_SDT.GetCountOfRecords
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_SDT::GetCountOfRecords


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfRecords</b> method returns the number of records in the SDT.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sdt">IDVB_SDT Interface</a>
 

 

