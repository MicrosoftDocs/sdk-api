---
UID: NF:dvbsiparser.IDVB_SDT.GetNextTable
title: IDVB_SDT::GetNextTable (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetNextTable","GetNextTable method [Microsoft TV Technologies]","GetNextTable method [Microsoft TV Technologies]","IDVB_SDT interface","IDVB_SDT interface [Microsoft TV Technologies]","GetNextTable method","IDVB_SDT.GetNextTable","IDVB_SDT::GetNextTable","IDVB_SDTGetNextTable","dvbsiparser/IDVB_SDT::GetNextTable","mstv.idvb_sdt_getnexttable"]
old-location: mstv\idvb_sdt_getnexttable.htm
tech.root: mstv
ms.assetid: c1bc015d-1ea2-4e68-8fbc-39e0bc973d01
ms.date: 12/05/2018
ms.keywords: GetNextTable, GetNextTable method [Microsoft TV Technologies], GetNextTable method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetNextTable method, IDVB_SDT.GetNextTable, IDVB_SDT::GetNextTable, IDVB_SDTGetNextTable, dvbsiparser/IDVB_SDT::GetNextTable, mstv.idvb_sdt_getnexttable
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
 - IDVB_SDT::GetNextTable
 - dvbsiparser/IDVB_SDT::GetNextTable
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
 - IDVB_SDT.GetNextTable
---

# IDVB_SDT::GetNextTable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetNextTable</b> method retrieves the <i>next</i> table that follows the current table.

## -parameters

### -param ppSDT [out]

Address of a variable that receives an <b>IDVB_SDT</b> interface pointer. The caller must release the interface.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This table is not current.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

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

This method applies only to <i>current</i> tables. Otherwise, the method returns E_ACCESSDENIED.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sdt">IDVB_SDT Interface</a>