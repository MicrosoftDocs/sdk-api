---
UID: NF:mpeg2psiparser.ITSDT.GetNextTable
title: ITSDT::GetNextTable (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["GetNextTable","GetNextTable method [Microsoft TV Technologies]","GetNextTable method [Microsoft TV Technologies]","ITSDT interface","ITSDT interface [Microsoft TV Technologies]","GetNextTable method","ITSDT.GetNextTable","ITSDT::GetNextTable","ITSDTGetNextTable","mpeg2psiparser/ITSDT::GetNextTable","mstv.itsdt_getnexttable"]
old-location: mstv\itsdt_getnexttable.htm
tech.root: mstv
ms.assetid: 7b60647a-b668-4884-967d-044ff0d149c2
ms.date: 12/05/2018
ms.keywords: GetNextTable, GetNextTable method [Microsoft TV Technologies], GetNextTable method [Microsoft TV Technologies],ITSDT interface, ITSDT interface [Microsoft TV Technologies],GetNextTable method, ITSDT.GetNextTable, ITSDT::GetNextTable, ITSDTGetNextTable, mpeg2psiparser/ITSDT::GetNextTable, mstv.itsdt_getnexttable
req.header: mpeg2psiparser.h
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
 - ITSDT::GetNextTable
 - mpeg2psiparser/ITSDT::GetNextTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - ITSDT.GetNextTable
---

# ITSDT::GetNextTable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetNextTable</b> method retrieves the <i>next</i> table that follows the current table.

## -parameters

### -param ppTSDT [out]

Address of a variable that receives an <b>ITSDT</b> interface pointer. The caller must release the interface.

## -returns

<table>
<tr>
<th>Return code
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>E_ACCESSDENIED</td>
<td>This table is not current.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>Failure.</td>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>

## -remarks

This method applies only to current tables. Otherwise, the method returns E_ACCESSDENIED.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-itsdt">ITSDT Interface</a>