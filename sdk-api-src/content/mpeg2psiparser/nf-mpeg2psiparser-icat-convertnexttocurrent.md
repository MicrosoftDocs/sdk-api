---
UID: NF:mpeg2psiparser.ICAT.ConvertNextToCurrent
title: ICAT::ConvertNextToCurrent (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["ConvertNextToCurrent","ConvertNextToCurrent method [Microsoft TV Technologies]","ConvertNextToCurrent method [Microsoft TV Technologies]","ICAT interface","ICAT interface [Microsoft TV Technologies]","ConvertNextToCurrent method","ICAT.ConvertNextToCurrent","ICAT::ConvertNextToCurrent","ICATConvertNextToCurrent","mpeg2psiparser/ICAT::ConvertNextToCurrent","mstv.icat_convertnexttocurrent"]
old-location: mstv\icat_convertnexttocurrent.htm
tech.root: mstv
ms.assetid: bdd8f7a6-0c77-4058-bcca-9d712da781e0
ms.date: 12/05/2018
ms.keywords: ConvertNextToCurrent, ConvertNextToCurrent method [Microsoft TV Technologies], ConvertNextToCurrent method [Microsoft TV Technologies],ICAT interface, ICAT interface [Microsoft TV Technologies],ConvertNextToCurrent method, ICAT.ConvertNextToCurrent, ICAT::ConvertNextToCurrent, ICATConvertNextToCurrent, mpeg2psiparser/ICAT::ConvertNextToCurrent, mstv.icat_convertnexttocurrent
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
 - ICAT::ConvertNextToCurrent
 - mpeg2psiparser/ICAT::ConvertNextToCurrent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mpeg2psiparser.h
api_name:
 - ICAT.ConvertNextToCurrent
---

# ICAT::ConvertNextToCurrent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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

This method applies only to <i>next</i> tables that have become current. Before calling this method, call <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-icat-registerforwhencurrent">ICAT::RegisterForWhenCurrent</a> and wait for the event to be signaled.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-icat">ICAT Interface</a>
