---
UID: NF:dvbsiparser.IDVB_ST.GetData
title: IDVB_ST::GetData (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetData","GetData method [Microsoft TV Technologies]","GetData method [Microsoft TV Technologies]","IDVB_ST interface","IDVB_ST interface [Microsoft TV Technologies]","GetData method","IDVB_ST.GetData","IDVB_ST::GetData","IDVB_STGetData","dvbsiparser/IDVB_ST::GetData","mstv.idvb_st_getdata"]
old-location: mstv\idvb_st_getdata.htm
tech.root: mstv
ms.assetid: 3afdafad-462c-4fad-a9c6-ec820bedf31a
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Microsoft TV Technologies], GetData method [Microsoft TV Technologies],IDVB_ST interface, IDVB_ST interface [Microsoft TV Technologies],GetData method, IDVB_ST.GetData, IDVB_ST::GetData, IDVB_STGetData, dvbsiparser/IDVB_ST::GetData, mstv.idvb_st_getdata
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
 - IDVB_ST::GetData
 - dvbsiparser/IDVB_ST::GetData
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
 - IDVB_ST.GetData
---

# IDVB_ST::GetData


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetData</b> method returns the data in the ST.

## -parameters

### -param ppData [out]

Address of a variable that receives a pointer to a buffer, which contains all of the data_byte fields in the ST. To get the size of the buffer, call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_st-getdatalength">IDVB_ST::GetDataLength</a> method. The caller must release the buffer by calling the <b>CoTaskMemFree</b> function.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The ST does not contain any data.

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

## -remarks

The data in an ST has no meaning.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_st">IDVB_ST Interface</a>