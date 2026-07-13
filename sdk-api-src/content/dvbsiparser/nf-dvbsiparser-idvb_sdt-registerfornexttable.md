---
UID: NF:dvbsiparser.IDVB_SDT.RegisterForNextTable
title: IDVB_SDT::RegisterForNextTable (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_SDT interface [Microsoft TV Technologies]","RegisterForNextTable method","IDVB_SDT.RegisterForNextTable","IDVB_SDT::RegisterForNextTable","IDVB_SDTRegisterForNextTable","RegisterForNextTable","RegisterForNextTable method [Microsoft TV Technologies]","RegisterForNextTable method [Microsoft TV Technologies]","IDVB_SDT interface","dvbsiparser/IDVB_SDT::RegisterForNextTable","mstv.idvb_sdt_registerfornexttable"]
old-location: mstv\idvb_sdt_registerfornexttable.htm
tech.root: mstv
ms.assetid: f8040b5a-004a-4428-9906-22aedcd780f6
ms.date: 12/05/2018
ms.keywords: IDVB_SDT interface [Microsoft TV Technologies],RegisterForNextTable method, IDVB_SDT.RegisterForNextTable, IDVB_SDT::RegisterForNextTable, IDVB_SDTRegisterForNextTable, RegisterForNextTable, RegisterForNextTable method [Microsoft TV Technologies], RegisterForNextTable method [Microsoft TV Technologies],IDVB_SDT interface, dvbsiparser/IDVB_SDT::RegisterForNextTable, mstv.idvb_sdt_registerfornexttable
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
 - IDVB_SDT::RegisterForNextTable
 - dvbsiparser/IDVB_SDT::RegisterForNextTable
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
 - IDVB_SDT.RegisterForNextTable
---

# IDVB_SDT::RegisterForNextTable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>RegisterForNextTable</b> method registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

## -parameters

### -param hNextTableAvailable [in]

Handle to an event created by the caller. The object signals the event when the <i>next</i> table arrives. When the event is signaled, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getnexttable">IDVB_SDT::GetNextTable</a> to retrieve the table.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sdt">IDVB_SDT Interface</a>