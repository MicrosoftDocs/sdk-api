---
UID: NF:dvbsiparser.IDVB_SIT.RegisterForWhenCurrent
title: IDVB_SIT::RegisterForWhenCurrent (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_SIT interface [Microsoft TV Technologies]","RegisterForWhenCurrent method","IDVB_SIT.RegisterForWhenCurrent","IDVB_SIT::RegisterForWhenCurrent","IDVB_SITRegisterForWhenCurrent","RegisterForWhenCurrent","RegisterForWhenCurrent method [Microsoft TV Technologies]","RegisterForWhenCurrent method [Microsoft TV Technologies]","IDVB_SIT interface","dvbsiparser/IDVB_SIT::RegisterForWhenCurrent","mstv.idvb_sit_registerforwhencurrent"]
old-location: mstv\idvb_sit_registerforwhencurrent.htm
tech.root: mstv
ms.assetid: a60fa143-0e02-4af8-a64f-1fc92f8e0a3f
ms.date: 12/05/2018
ms.keywords: IDVB_SIT interface [Microsoft TV Technologies],RegisterForWhenCurrent method, IDVB_SIT.RegisterForWhenCurrent, IDVB_SIT::RegisterForWhenCurrent, IDVB_SITRegisterForWhenCurrent, RegisterForWhenCurrent, RegisterForWhenCurrent method [Microsoft TV Technologies], RegisterForWhenCurrent method [Microsoft TV Technologies],IDVB_SIT interface, dvbsiparser/IDVB_SIT::RegisterForWhenCurrent, mstv.idvb_sit_registerforwhencurrent
f1_keywords:
- dvbsiparser/IDVB_SIT.RegisterForWhenCurrent
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
- IDVB_SIT.RegisterForWhenCurrent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_SIT::RegisterForWhenCurrent


## -description



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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sit">IDVB_SIT Interface</a>
 

 

