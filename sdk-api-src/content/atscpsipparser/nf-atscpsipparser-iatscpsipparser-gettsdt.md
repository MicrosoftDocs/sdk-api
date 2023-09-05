---
UID: NF:atscpsipparser.IAtscPsipParser.GetTSDT
title: IAtscPsipParser::GetTSDT (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetTSDT","GetTSDT method [Microsoft TV Technologies]","GetTSDT method [Microsoft TV Technologies]","IAtscPsipParser interface","IAtscPsipParser interface [Microsoft TV Technologies]","GetTSDT method","IAtscPsipParser.GetTSDT","IAtscPsipParser::GetTSDT","IAtscPsipParserGetTSDT","atscpsipparser/IAtscPsipParser::GetTSDT","mstv.iatscpsipparser_gettsdt"]
old-location: mstv\iatscpsipparser_gettsdt.htm
tech.root: mstv
ms.assetid: f9c25b9e-615d-4223-baf5-f4df2fc1473a
ms.date: 12/05/2018
ms.keywords: GetTSDT, GetTSDT method [Microsoft TV Technologies], GetTSDT method [Microsoft TV Technologies],IAtscPsipParser interface, IAtscPsipParser interface [Microsoft TV Technologies],GetTSDT method, IAtscPsipParser.GetTSDT, IAtscPsipParser::GetTSDT, IAtscPsipParserGetTSDT, atscpsipparser/IAtscPsipParser::GetTSDT, mstv.iatscpsipparser_gettsdt
req.header: atscpsipparser.h
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
 - IAtscPsipParser::GetTSDT
 - atscpsipparser/IAtscPsipParser::GetTSDT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IAtscPsipParser.GetTSDT
---

# IAtscPsipParser::GetTSDT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTSDT</b> method retrieves the transport stream description table (TSDT).

## -parameters

### -param ppTSDT [out]

Receives an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-itsdt">ITSDT</a> interface pointer. The caller must release the interface.

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
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <b>Initialize</b> method was not called.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatscpsipparser">IAtscPsipParser Interface</a>