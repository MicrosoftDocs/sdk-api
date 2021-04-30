---
UID: NF:dvbsiparser.IDVB_NIT.GetRecordOriginalNetworkId
title: IDVB_NIT::GetRecordOriginalNetworkId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordOriginalNetworkId","GetRecordOriginalNetworkId method [Microsoft TV Technologies]","GetRecordOriginalNetworkId method [Microsoft TV Technologies]","IDVB_NIT interface","IDVB_NIT interface [Microsoft TV Technologies]","GetRecordOriginalNetworkId method","IDVB_NIT.GetRecordOriginalNetworkId","IDVB_NIT::GetRecordOriginalNetworkId","IDVB_NITGetRecordOriginalNetworkId","dvbsiparser/IDVB_NIT::GetRecordOriginalNetworkId","mstv.idvb_nit_getrecordoriginalnetworkid"]
old-location: mstv\idvb_nit_getrecordoriginalnetworkid.htm
tech.root: mstv
ms.assetid: 3179be9a-de2d-4cb3-ace2-ad5af66d35c8
ms.date: 12/05/2018
ms.keywords: GetRecordOriginalNetworkId, GetRecordOriginalNetworkId method [Microsoft TV Technologies], GetRecordOriginalNetworkId method [Microsoft TV Technologies],IDVB_NIT interface, IDVB_NIT interface [Microsoft TV Technologies],GetRecordOriginalNetworkId method, IDVB_NIT.GetRecordOriginalNetworkId, IDVB_NIT::GetRecordOriginalNetworkId, IDVB_NITGetRecordOriginalNetworkId, dvbsiparser/IDVB_NIT::GetRecordOriginalNetworkId, mstv.idvb_nit_getrecordoriginalnetworkid
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
 - IDVB_NIT::GetRecordOriginalNetworkId
 - dvbsiparser/IDVB_NIT::GetRecordOriginalNetworkId
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
 - IDVB_NIT.GetRecordOriginalNetworkId
---

# IDVB_NIT::GetRecordOriginalNetworkId


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordOriginalNetworkId</b> method returns the original network identifier for a record in the NIT.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_nit-getcountofrecords">IDVB_NIT::GetCountOfRecords</a> method to get the number of records in the NIT.

### -param pwVal [out]

Pointer to a variable that receives the original_network_id field. This value identifies the network_id of the originating delivery system.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_nit">IDVB_NIT Interface</a>