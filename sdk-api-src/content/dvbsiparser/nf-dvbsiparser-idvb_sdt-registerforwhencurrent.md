---
UID: NF:dvbsiparser.IDVB_SDT.RegisterForWhenCurrent
title: IDVB_SDT::RegisterForWhenCurrent (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_SDT interface [Microsoft TV Technologies]","RegisterForWhenCurrent method","IDVB_SDT.RegisterForWhenCurrent","IDVB_SDT::RegisterForWhenCurrent","IDVB_SDTRegisterForWhenCurrent","RegisterForWhenCurrent","RegisterForWhenCurrent method [Microsoft TV Technologies]","RegisterForWhenCurrent method [Microsoft TV Technologies]","IDVB_SDT interface","dvbsiparser/IDVB_SDT::RegisterForWhenCurrent","mstv.idvb_sdt_registerforwhencurrent"]
old-location: mstv\idvb_sdt_registerforwhencurrent.htm
tech.root: mstv
ms.assetid: 240238fb-54fc-4465-b4dd-4878f43c50a9
ms.date: 12/05/2018
ms.keywords: IDVB_SDT interface [Microsoft TV Technologies],RegisterForWhenCurrent method, IDVB_SDT.RegisterForWhenCurrent, IDVB_SDT::RegisterForWhenCurrent, IDVB_SDTRegisterForWhenCurrent, RegisterForWhenCurrent, RegisterForWhenCurrent method [Microsoft TV Technologies], RegisterForWhenCurrent method [Microsoft TV Technologies],IDVB_SDT interface, dvbsiparser/IDVB_SDT::RegisterForWhenCurrent, mstv.idvb_sdt_registerforwhencurrent
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
 - IDVB_SDT::RegisterForWhenCurrent
 - dvbsiparser/IDVB_SDT::RegisterForWhenCurrent
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
 - IDVB_SDT.RegisterForWhenCurrent
---

# IDVB_SDT::RegisterForWhenCurrent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sdt">IDVB_SDT Interface</a>