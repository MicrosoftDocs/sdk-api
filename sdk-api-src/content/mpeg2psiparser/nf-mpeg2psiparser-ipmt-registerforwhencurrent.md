---
UID: NF:mpeg2psiparser.IPMT.RegisterForWhenCurrent
title: IPMT::RegisterForWhenCurrent (mpeg2psiparser.h)
description: The RegisterForWhenCurrent method registers the client to be notified when the table becomes current.
helpviewer_keywords: ["IPMT interface [Microsoft TV Technologies]","RegisterForWhenCurrent method","IPMT.RegisterForWhenCurrent","IPMT::RegisterForWhenCurrent","IPMTRegisterForWhenCurrent","RegisterForWhenCurrent","RegisterForWhenCurrent method [Microsoft TV Technologies]","RegisterForWhenCurrent method [Microsoft TV Technologies]","IPMT interface","mpeg2psiparser/IPMT::RegisterForWhenCurrent","mstv.ipmt_registerforwhencurrent"]
old-location: mstv\ipmt_registerforwhencurrent.htm
tech.root: mstv
ms.assetid: 4759c813-3a1f-492a-bca9-cb6610f6426b
ms.date: 12/05/2018
ms.keywords: IPMT interface [Microsoft TV Technologies],RegisterForWhenCurrent method, IPMT.RegisterForWhenCurrent, IPMT::RegisterForWhenCurrent, IPMTRegisterForWhenCurrent, RegisterForWhenCurrent, RegisterForWhenCurrent method [Microsoft TV Technologies], RegisterForWhenCurrent method [Microsoft TV Technologies],IPMT interface, mpeg2psiparser/IPMT::RegisterForWhenCurrent, mstv.ipmt_registerforwhencurrent
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
 - IPMT::RegisterForWhenCurrent
 - mpeg2psiparser/IPMT::RegisterForWhenCurrent
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
 - IPMT.RegisterForWhenCurrent
---

# IPMT::RegisterForWhenCurrent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>RegisterForWhenCurrent</b> method registers the client to be notified when the table becomes current.

## -parameters

### -param hNextTableIsCurrent [in]

Handle to an event created by the caller. The object signals the event when the table becomes current.

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
This table is already a <i>current</i> table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>hNextTableIsCurrent</i> cannot be <b>NULL</b>.

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

This method applies only to <i>next</i> tables. Otherwise, the method returns E_ACCESSDENIED.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>