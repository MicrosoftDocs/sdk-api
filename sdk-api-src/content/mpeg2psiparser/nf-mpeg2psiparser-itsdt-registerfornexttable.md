---
UID: NF:mpeg2psiparser.ITSDT.RegisterForNextTable
title: ITSDT::RegisterForNextTable (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["ITSDT interface [Microsoft TV Technologies]","RegisterForNextTable method","ITSDT.RegisterForNextTable","ITSDT::RegisterForNextTable","ITSDTRegisterForNextTable","RegisterForNextTable","RegisterForNextTable method [Microsoft TV Technologies]","RegisterForNextTable method [Microsoft TV Technologies]","ITSDT interface","mpeg2psiparser/ITSDT::RegisterForNextTable","mstv.itsdt_registerfornexttable"]
old-location: mstv\itsdt_registerfornexttable.htm
tech.root: mstv
ms.assetid: 36d597e2-0a65-48f3-8220-bb3481185af7
ms.date: 12/05/2018
ms.keywords: ITSDT interface [Microsoft TV Technologies],RegisterForNextTable method, ITSDT.RegisterForNextTable, ITSDT::RegisterForNextTable, ITSDTRegisterForNextTable, RegisterForNextTable, RegisterForNextTable method [Microsoft TV Technologies], RegisterForNextTable method [Microsoft TV Technologies],ITSDT interface, mpeg2psiparser/ITSDT::RegisterForNextTable, mstv.itsdt_registerfornexttable
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
 - ITSDT::RegisterForNextTable
 - mpeg2psiparser/ITSDT::RegisterForNextTable
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
 - ITSDT.RegisterForNextTable
---

# ITSDT::RegisterForNextTable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>RegisterForNextTable</b> method registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

## -parameters

### -param hNextTableAvailable [in]

Handle to an event created by the caller. The object signals the event when the <i>next</i> table arrives. When the event is signaled, call the <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-itsdt-getnexttable">ITSDT::GetNextTable</a> method to retrieve the table.

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
This table is already a <i>next</i> table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>hNextTableAvailable</i> cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The method has already been called.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-itsdt">ITSDT Interface</a>