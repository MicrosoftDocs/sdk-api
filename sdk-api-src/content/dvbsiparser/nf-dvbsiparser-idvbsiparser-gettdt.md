---
UID: NF:dvbsiparser.IDvbSiParser.GetTDT
title: IDvbSiParser::GetTDT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetTDT","GetTDT method [Microsoft TV Technologies]","GetTDT method [Microsoft TV Technologies]","IDvbSiParser interface","IDvbSiParser interface [Microsoft TV Technologies]","GetTDT method","IDvbSiParser.GetTDT","IDvbSiParser::GetTDT","IDvbSiParserGetTDT","dvbsiparser/IDvbSiParser::GetTDT","mstv.idvbsiparser_gettdt"]
old-location: mstv\idvbsiparser_gettdt.htm
tech.root: mstv
ms.assetid: 0922ccda-7bd8-480d-8cd1-64f170b7ec69
ms.date: 12/05/2018
ms.keywords: GetTDT, GetTDT method [Microsoft TV Technologies], GetTDT method [Microsoft TV Technologies],IDvbSiParser interface, IDvbSiParser interface [Microsoft TV Technologies],GetTDT method, IDvbSiParser.GetTDT, IDvbSiParser::GetTDT, IDvbSiParserGetTDT, dvbsiparser/IDvbSiParser::GetTDT, mstv.idvbsiparser_gettdt
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
 - IDvbSiParser::GetTDT
 - dvbsiparser/IDvbSiParser::GetTDT
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
 - IDvbSiParser.GetTDT
---

# IDvbSiParser::GetTDT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTDT</b> method retrieves the time and date table (TDT).

## -parameters

### -param ppTDT [out]

Address of a variable that receives an <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_tdt">IDVB_TDT</a> interface pointer. The caller must release the interface.

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
<dt><b>MPEG2_E_SECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The filter did not receive the table in the allotted time.

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

The method fails if the filter does not receive a matching table within a predetermined length of time.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsiparser">IDvbSiParser Interface</a>