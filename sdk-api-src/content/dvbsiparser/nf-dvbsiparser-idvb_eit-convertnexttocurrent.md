---
UID: NF:dvbsiparser.IDVB_EIT.ConvertNextToCurrent
title: IDVB_EIT::ConvertNextToCurrent (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["ConvertNextToCurrent","ConvertNextToCurrent method [Microsoft TV Technologies]","ConvertNextToCurrent method [Microsoft TV Technologies]","IDVB_EIT interface","IDVB_EIT interface [Microsoft TV Technologies]","ConvertNextToCurrent method","IDVB_EIT.ConvertNextToCurrent","IDVB_EIT::ConvertNextToCurrent","IDVB_EITConvertNextToCurrent","dvbsiparser/IDVB_EIT::ConvertNextToCurrent","mstv.idvb_eit_convertnexttocurrent"]
old-location: mstv\idvb_eit_convertnexttocurrent.htm
tech.root: mstv
ms.assetid: 634be949-4918-4cae-a282-54cf036d3a09
ms.date: 12/05/2018
ms.keywords: ConvertNextToCurrent, ConvertNextToCurrent method [Microsoft TV Technologies], ConvertNextToCurrent method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],ConvertNextToCurrent method, IDVB_EIT.ConvertNextToCurrent, IDVB_EIT::ConvertNextToCurrent, IDVB_EITConvertNextToCurrent, dvbsiparser/IDVB_EIT::ConvertNextToCurrent, mstv.idvb_eit_convertnexttocurrent
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
 - IDVB_EIT::ConvertNextToCurrent
 - dvbsiparser/IDVB_EIT::ConvertNextToCurrent
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
 - IDVB_EIT.ConvertNextToCurrent
---

# IDVB_EIT::ConvertNextToCurrent


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>ConvertNextToCurrent</b> method converts a <i>next</i> table to a <i>current</i> table.



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
This table is already current.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <b>RegisterForWhenCurrent</b> method was not called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
The new <i>current</i> table is malformed.

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

This method applies only to <i>next</i> tables that have become current. Before calling this method, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-registerforwhencurrent">IDVB_EIT::RegisterForWhenCurrent</a> and wait for the event to be signaled.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT Interface</a>
