---
UID: NF:tapi3cc.ITACDGroupEvent.get_Group
title: ITACDGroupEvent::get_Group (tapi3cc.h)
description: The ITACDGroupEvent::get_Group method (tapi3cc.h) gets the ITACDGroup interface pointer for the group on which the event occurred.
helpviewer_keywords: ["ITACDGroupEvent interface [TAPI 2.2]","get_Group method","ITACDGroupEvent.get_Group","ITACDGroupEvent::get_Group","_tapi3_itacdgroupevent_get_group","get_Group","get_Group method [TAPI 2.2]","get_Group method [TAPI 2.2]","ITACDGroupEvent interface","tapi3.itacdgroupevent_get_group","tapi3cc/ITACDGroupEvent::get_Group"]
old-location: tapi3\itacdgroupevent_get_group.htm
tech.root: tapi3
ms.assetid: bbdc94b0-fa46-422a-bffc-32bbd1d49e5a
ms.date: 08/09/2022
ms.keywords: ITACDGroupEvent interface [TAPI 2.2],get_Group method, ITACDGroupEvent.get_Group, ITACDGroupEvent::get_Group, _tapi3_itacdgroupevent_get_group, get_Group, get_Group method [TAPI 2.2], get_Group method [TAPI 2.2],ITACDGroupEvent interface, tapi3.itacdgroupevent_get_group, tapi3cc/ITACDGroupEvent::get_Group
req.header: tapi3cc.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITACDGroupEvent::get_Group
 - tapi3cc/ITACDGroupEvent::get_Group
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITACDGroupEvent.get_Group
---

# ITACDGroupEvent::get_Group


## -description

The 
<b>get_Group</b> method gets the ITACDGroup interface pointer for the group on which the event occurred.

## -parameters

### -param ppGroup [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> interface on which the event occurred.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppGroup</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> interface returned by <b>ITACDGroupEvent::get_Group</b>. The application must call <b>Release</b> on the 
<b>ITACDGroup</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroupevent">ITACDGroupEvent</a>
