---
UID: NF:dvbsiparser.IDvbSiParser.GetEIT
title: IDvbSiParser::GetEIT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetEIT","GetEIT method [Microsoft TV Technologies]","GetEIT method [Microsoft TV Technologies]","IDvbSiParser interface","IDvbSiParser interface [Microsoft TV Technologies]","GetEIT method","IDvbSiParser.GetEIT","IDvbSiParser::GetEIT","IDvbSiParserGetEIT","dvbsiparser/IDvbSiParser::GetEIT","mstv.idvbsiparser_geteit"]
old-location: mstv\idvbsiparser_geteit.htm
tech.root: mstv
ms.assetid: fd1c0418-2bec-4270-be4b-3877428e3968
ms.date: 12/05/2018
ms.keywords: GetEIT, GetEIT method [Microsoft TV Technologies], GetEIT method [Microsoft TV Technologies],IDvbSiParser interface, IDvbSiParser interface [Microsoft TV Technologies],GetEIT method, IDvbSiParser.GetEIT, IDvbSiParser::GetEIT, IDvbSiParserGetEIT, dvbsiparser/IDvbSiParser::GetEIT, mstv.idvbsiparser_geteit
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
 - IDvbSiParser::GetEIT
 - dvbsiparser/IDvbSiParser::GetEIT
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
 - IDvbSiParser.GetEIT
---

# IDvbSiParser::GetEIT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetEIT</b> method retrieves the event information table (EIT).

## -parameters

### -param tableId [in]

Specifies the table identifier of the EIT. Use one of the values in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>DVB_EIT_ACTUAL_TID (0x4E)</td>
<td>Present/following EIT for this transport stream.</td>
</tr>
<tr>
<td>DVB_EIT_OTHER_TID (0x4F)</td>
<td>Present/following EIT for another transport stream.</td>
</tr>
<tr>
<td>0x50 – 0x5F</td>
<td>Schedule EIT for this transport stream.</td>
</tr>
<tr>
<td>0x60 – 0x6F</td>
<td>Schedule EIT for another transport stream.</td>
</tr>
</table>

### -param pwServiceId [in]

Optional parameter that contains a service identifier. You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.

### -param ppEIT [out]

Address of a variable that receives an <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT</a> interface pointer. The caller must release the interface.

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