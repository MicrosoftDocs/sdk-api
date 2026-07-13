---
UID: NF:dvbsiparser.IDvbSiParser.GetCAT
title: IDvbSiParser::GetCAT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCAT","GetCAT method [Microsoft TV Technologies]","GetCAT method [Microsoft TV Technologies]","IDvbSiParser interface","IDvbSiParser interface [Microsoft TV Technologies]","GetCAT method","IDvbSiParser.GetCAT","IDvbSiParser::GetCAT","IDvbSiParserGetCAT","dvbsiparser/IDvbSiParser::GetCAT","mstv.idvbsiparser_getcat"]
old-location: mstv\idvbsiparser_getcat.htm
tech.root: mstv
ms.assetid: afd6286a-1b05-408f-a752-6fc3a2667e31
ms.date: 12/05/2018
ms.keywords: GetCAT, GetCAT method [Microsoft TV Technologies], GetCAT method [Microsoft TV Technologies],IDvbSiParser interface, IDvbSiParser interface [Microsoft TV Technologies],GetCAT method, IDvbSiParser.GetCAT, IDvbSiParser::GetCAT, IDvbSiParserGetCAT, dvbsiparser/IDvbSiParser::GetCAT, mstv.idvbsiparser_getcat
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
 - IDvbSiParser::GetCAT
 - dvbsiparser/IDvbSiParser::GetCAT
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
 - IDvbSiParser.GetCAT
---

# IDvbSiParser::GetCAT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCAT</b> method retrieves the conditional access table (CAT).

## -parameters

### -param dwTimeout [in]

Specifies a time-out value, in milliseconds. If the filter does not receive the data within the time-out period, the method fails.

### -param ppCAT [out]

Address of a variable that receives an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-icat">ICAT</a> interface pointer. The caller must release the interface.

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

The method returns the first CAT that is marked <i>current</i>; that is, one in which the current_next_indicator bit is 1.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsiparser">IDvbSiParser Interface</a>