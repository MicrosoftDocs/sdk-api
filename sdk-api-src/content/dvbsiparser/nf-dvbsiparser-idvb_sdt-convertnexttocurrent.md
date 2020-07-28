---
UID: NF:dvbsiparser.IDVB_SDT.ConvertNextToCurrent
title: IDVB_SDT::ConvertNextToCurrent (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["ConvertNextToCurrent","ConvertNextToCurrent method [Microsoft TV Technologies]","ConvertNextToCurrent method [Microsoft TV Technologies]","IDVB_SDT interface","IDVB_SDT interface [Microsoft TV Technologies]","ConvertNextToCurrent method","IDVB_SDT.ConvertNextToCurrent","IDVB_SDT::ConvertNextToCurrent","IDVB_SDTConvertNextToCurrent","dvbsiparser/IDVB_SDT::ConvertNextToCurrent","mstv.idvb_sdt_convertnexttocurrent"]
old-location: mstv\idvb_sdt_convertnexttocurrent.htm
tech.root: mstv
ms.assetid: 05cddb06-1edb-4514-b6fc-21e920e469ea
ms.date: 12/05/2018
ms.keywords: ConvertNextToCurrent, ConvertNextToCurrent method [Microsoft TV Technologies], ConvertNextToCurrent method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],ConvertNextToCurrent method, IDVB_SDT.ConvertNextToCurrent, IDVB_SDT::ConvertNextToCurrent, IDVB_SDTConvertNextToCurrent, dvbsiparser/IDVB_SDT::ConvertNextToCurrent, mstv.idvb_sdt_convertnexttocurrent
f1_keywords:
- dvbsiparser/IDVB_SDT.ConvertNextToCurrent
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IDVB_SDT.ConvertNextToCurrent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_SDT::ConvertNextToCurrent


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>ConvertNextToCurrent</b> method converts a <i>next</i> table to a <i>current</i> table.


## -parameters






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



This method applies only to <i>next</i> tables that have become current. Before calling this method, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-registerforwhencurrent">IDVB_SDT::RegisterForWhenCurrent</a> and wait for the event to be signaled.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sdt">IDVB_SDT Interface</a>
 

 

