---
UID: NF:dvbsiparser.IDVB_ST.GetDataLength
title: IDVB_ST::GetDataLength (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetDataLength","GetDataLength method [Microsoft TV Technologies]","GetDataLength method [Microsoft TV Technologies]","IDVB_ST interface","IDVB_ST interface [Microsoft TV Technologies]","GetDataLength method","IDVB_ST.GetDataLength","IDVB_ST::GetDataLength","IDVB_STGetDataLength","dvbsiparser/IDVB_ST::GetDataLength","mstv.idvb_st_getdatalength"]
old-location: mstv\idvb_st_getdatalength.htm
tech.root: mstv
ms.assetid: 6d42f147-b82d-4236-9e58-c42019d6b413
ms.date: 12/05/2018
ms.keywords: GetDataLength, GetDataLength method [Microsoft TV Technologies], GetDataLength method [Microsoft TV Technologies],IDVB_ST interface, IDVB_ST interface [Microsoft TV Technologies],GetDataLength method, IDVB_ST.GetDataLength, IDVB_ST::GetDataLength, IDVB_STGetDataLength, dvbsiparser/IDVB_ST::GetDataLength, mstv.idvb_st_getdatalength
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
 - IDVB_ST::GetDataLength
 - dvbsiparser/IDVB_ST::GetDataLength
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
 - IDVB_ST.GetDataLength
---

# IDVB_ST::GetDataLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetDataLength</b> method returns the length of the data in the ST.

## -parameters

### -param pwVal [out]

Pointer to a variable that receives the length, in bytes.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_st">IDVB_ST Interface</a>