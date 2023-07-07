---
UID: NF:dvbsiparser.IDvbSiParser.GetSDT
title: IDvbSiParser::GetSDT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetSDT","GetSDT method [Microsoft TV Technologies]","GetSDT method [Microsoft TV Technologies]","IDvbSiParser interface","IDvbSiParser interface [Microsoft TV Technologies]","GetSDT method","IDvbSiParser.GetSDT","IDvbSiParser::GetSDT","IDvbSiParserGetSDT","dvbsiparser/IDvbSiParser::GetSDT","mstv.idvbsiparser_getsdt"]
old-location: mstv\idvbsiparser_getsdt.htm
tech.root: mstv
ms.assetid: 65fe8b2d-31b2-4335-8f5d-9c601e2a64e5
ms.date: 12/05/2018
ms.keywords: GetSDT, GetSDT method [Microsoft TV Technologies], GetSDT method [Microsoft TV Technologies],IDvbSiParser interface, IDvbSiParser interface [Microsoft TV Technologies],GetSDT method, IDvbSiParser.GetSDT, IDvbSiParser::GetSDT, IDvbSiParserGetSDT, dvbsiparser/IDvbSiParser::GetSDT, mstv.idvbsiparser_getsdt
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
 - IDvbSiParser::GetSDT
 - dvbsiparser/IDvbSiParser::GetSDT
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
 - IDvbSiParser.GetSDT
---

# IDvbSiParser::GetSDT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetSDT</b> method retrieves the service description table (SDT).

## -parameters

### -param tableId [in]

Specifies the table identifier of the SDT. Use one of the values in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>DVB_SDT_ACTUAL_TID (0x42)</td>
<td>SDT for the current transport stream.</td>
</tr>
<tr>
<td>DVB_SDT_OTHER_TID (0x46)</td>
<td>SDT for another transport stream.</td>
</tr>
</table>

### -param pwTransportStreamId [in]

Optional parameter that contains a transport stream identifier (TSID). You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.

### -param ppSDT [out]

Address of a variable that receives an <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sdt">IDVB_SDT</a> interface pointer. The caller must release the interface.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
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