---
UID: NF:dvbsiparser.IDvbSiParser.GetPMT
title: IDvbSiParser::GetPMT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetPMT","GetPMT method [Microsoft TV Technologies]","GetPMT method [Microsoft TV Technologies]","IDvbSiParser interface","IDvbSiParser interface [Microsoft TV Technologies]","GetPMT method","IDvbSiParser.GetPMT","IDvbSiParser::GetPMT","IDvbSiParserGetPMT","dvbsiparser/IDvbSiParser::GetPMT","mstv.idvbsiparser_getpmt"]
old-location: mstv\idvbsiparser_getpmt.htm
tech.root: mstv
ms.assetid: cb8f21f4-fa03-4006-8563-2026e70d5f43
ms.date: 12/05/2018
ms.keywords: GetPMT, GetPMT method [Microsoft TV Technologies], GetPMT method [Microsoft TV Technologies],IDvbSiParser interface, IDvbSiParser interface [Microsoft TV Technologies],GetPMT method, IDvbSiParser.GetPMT, IDvbSiParser::GetPMT, IDvbSiParserGetPMT, dvbsiparser/IDvbSiParser::GetPMT, mstv.idvbsiparser_getpmt
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
 - IDvbSiParser::GetPMT
 - dvbsiparser/IDvbSiParser::GetPMT
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
 - IDvbSiParser.GetPMT
---

# IDvbSiParser::GetPMT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetPMT</b> method retrieves the program map table (PMT) for a specified packet identifier (PID).

## -parameters

### -param pid [in]

Specifies the PID for the requested PMT.

### -param pwProgramNumber [in]

Optional pointer to a variable that contains a table program number. You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.

### -param ppPMT [out]

Address of a variable that receives an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT</a> interface pointer. The caller must release the interface.

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
<b>NULL</b> pointer argument.

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