---
UID: NF:mpeg2psiparser.IPMT.RegisterForNextTable
title: IPMT::RegisterForNextTable (mpeg2psiparser.h)
description: The RegisterForNextTable method registers the client to be notified when a next table arrives that will replace the current table.
helpviewer_keywords: ["IPMT interface [Microsoft TV Technologies]","RegisterForNextTable method","IPMT.RegisterForNextTable","IPMT::RegisterForNextTable","IPMTRegisterForNextTable","RegisterForNextTable","RegisterForNextTable method [Microsoft TV Technologies]","RegisterForNextTable method [Microsoft TV Technologies]","IPMT interface","mpeg2psiparser/IPMT::RegisterForNextTable","mstv.ipmt_registerfornexttable"]
old-location: mstv\ipmt_registerfornexttable.htm
tech.root: mstv
ms.assetid: 6794c94a-8efe-4d53-a4f4-e25d14644270
ms.date: 12/05/2018
ms.keywords: IPMT interface [Microsoft TV Technologies],RegisterForNextTable method, IPMT.RegisterForNextTable, IPMT::RegisterForNextTable, IPMTRegisterForNextTable, RegisterForNextTable, RegisterForNextTable method [Microsoft TV Technologies], RegisterForNextTable method [Microsoft TV Technologies],IPMT interface, mpeg2psiparser/IPMT::RegisterForNextTable, mstv.ipmt_registerfornexttable
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
 - IPMT::RegisterForNextTable
 - mpeg2psiparser/IPMT::RegisterForNextTable
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
 - IPMT.RegisterForNextTable
---

# IPMT::RegisterForNextTable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>RegisterForNextTable</b> method registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

## -parameters

### -param hNextTableAvailable [in]

Handle to an event created by the caller. The object signals the event when the <i>next</i> table arrives. When the event is signaled, call the <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getnexttable">IPMT::GetNextTable</a> method to retrieve the table.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>