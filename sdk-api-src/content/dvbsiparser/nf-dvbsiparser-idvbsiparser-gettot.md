---
UID: NF:dvbsiparser.IDvbSiParser.GetTOT
title: IDvbSiParser::GetTOT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetTOT","GetTOT method [Microsoft TV Technologies]","GetTOT method [Microsoft TV Technologies]","IDvbSiParser interface","IDvbSiParser interface [Microsoft TV Technologies]","GetTOT method","IDvbSiParser.GetTOT","IDvbSiParser::GetTOT","IDvbSiParserGetTOT","dvbsiparser/IDvbSiParser::GetTOT","mstv.idvbsiparser_gettot"]
old-location: mstv\idvbsiparser_gettot.htm
tech.root: mstv
ms.assetid: 07e27472-2cb9-4bb1-9976-200bcdccb539
ms.date: 12/05/2018
ms.keywords: GetTOT, GetTOT method [Microsoft TV Technologies], GetTOT method [Microsoft TV Technologies],IDvbSiParser interface, IDvbSiParser interface [Microsoft TV Technologies],GetTOT method, IDvbSiParser.GetTOT, IDvbSiParser::GetTOT, IDvbSiParserGetTOT, dvbsiparser/IDvbSiParser::GetTOT, mstv.idvbsiparser_gettot
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
 - IDvbSiParser::GetTOT
 - dvbsiparser/IDvbSiParser::GetTOT
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
 - IDvbSiParser.GetTOT
---

# IDvbSiParser::GetTOT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTOT</b> method retrieves the time offset table (TOT).

## -parameters

### -param ppTOT [out]

Address of a variable that receives an <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_tot">IDVB_TOT</a> interface pointer. The caller must release the interface.

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