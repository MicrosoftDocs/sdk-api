---
UID: NF:dvbsiparser.IDVB_RST.GetRecordOriginalNetworkId
title: IDVB_RST::GetRecordOriginalNetworkId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetRecordOriginalNetworkId","GetRecordOriginalNetworkId method [Microsoft TV Technologies]","GetRecordOriginalNetworkId method [Microsoft TV Technologies]","IDVB_RST interface","IDVB_RST interface [Microsoft TV Technologies]","GetRecordOriginalNetworkId method","IDVB_RST.GetRecordOriginalNetworkId","IDVB_RST::GetRecordOriginalNetworkId","IDVB_RSTGetRecordOriginalNetworkId","dvbsiparser/IDVB_RST::GetRecordOriginalNetworkId","mstv.idvb_rst_getrecordoriginalnetworkid"]
old-location: mstv\idvb_rst_getrecordoriginalnetworkid.htm
tech.root: mstv
ms.assetid: 949dafeb-f59d-4507-a3eb-4a381f4108ff
ms.date: 12/05/2018
ms.keywords: GetRecordOriginalNetworkId, GetRecordOriginalNetworkId method [Microsoft TV Technologies], GetRecordOriginalNetworkId method [Microsoft TV Technologies],IDVB_RST interface, IDVB_RST interface [Microsoft TV Technologies],GetRecordOriginalNetworkId method, IDVB_RST.GetRecordOriginalNetworkId, IDVB_RST::GetRecordOriginalNetworkId, IDVB_RSTGetRecordOriginalNetworkId, dvbsiparser/IDVB_RST::GetRecordOriginalNetworkId, mstv.idvb_rst_getrecordoriginalnetworkid
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
 - IDVB_RST::GetRecordOriginalNetworkId
 - dvbsiparser/IDVB_RST::GetRecordOriginalNetworkId
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
 - IDVB_RST.GetRecordOriginalNetworkId
---

# IDVB_RST::GetRecordOriginalNetworkId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordOriginalNetworkId</b> method returns the original network identifier for a record in the RST.

## -parameters

### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getcountofrecords">IDVB_RST::GetCountOfRecords</a> method to get the number of records in the RST.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_rst">IDVB_RST Interface</a>