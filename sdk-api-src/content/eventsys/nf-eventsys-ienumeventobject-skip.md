---
UID: NF:eventsys.IEnumEventObject.Skip
title: IEnumEventObject::Skip (eventsys.h)
description: Skips over the specified number of items in the enumeration sequence. (IEnumEventObject.Skip)
helpviewer_keywords: ["IEnumEventObject interface [COM+]","Skip method","IEnumEventObject.Skip","IEnumEventObject::Skip","Skip","Skip method [COM+]","Skip method [COM+]","IEnumEventObject interface","_cos_ienumeventobject_skip","cos.ienumeventobject_skip","eventsys/IEnumEventObject::Skip"]
old-location: cos\ienumeventobject_skip.htm
tech.root: cos
ms.assetid: 7c830d29-8e66-4139-9445-d83dc7f7004f
ms.date: 12/05/2018
ms.keywords: IEnumEventObject interface [COM+],Skip method, IEnumEventObject.Skip, IEnumEventObject::Skip, Skip, Skip method [COM+], Skip method [COM+],IEnumEventObject interface, _cos_ienumeventobject_skip, cos.ienumeventobject_skip, eventsys/IEnumEventObject::Skip
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Eventsys.idl
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
 - IEnumEventObject::Skip
 - eventsys/IEnumEventObject::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - eventsys.h
api_name:
 - IEnumEventObject.Skip
---

# IEnumEventObject::Skip


## -description

Skips over the specified number of items in the enumeration sequence.

## -parameters

### -param cSkipElem [in]

The number of elements to be skipped.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The requested number of elements was skipped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of elements skipped was not the same as the number requested.

</td>
</tr>
</table>

## -remarks

<b>Skip</b> may return S_FALSE if <i>cSkipElem</i> is greater than the remaining number of elements. In this case, <b>Skip</b> moves to the last element in the enumeration sequence.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ienumeventobject">IEnumEventObject</a>
