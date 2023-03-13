---
UID: NF:eventsys.IEnumEventObject.Next
title: IEnumEventObject::Next (eventsys.h)
description: Retrieves the specified number of items in the enumeration sequence. (IEnumEventObject.Next)
helpviewer_keywords: ["IEnumEventObject interface [COM+]","Next method","IEnumEventObject.Next","IEnumEventObject::Next","Next","Next method [COM+]","Next method [COM+]","IEnumEventObject interface","_cos_ienumeventobject_next","cos.ienumeventobject_next","eventsys/IEnumEventObject::Next"]
old-location: cos\ienumeventobject_next.htm
tech.root: cos
ms.assetid: c9dab0b5-dbbb-4330-afd2-e13e708d708f
ms.date: 12/05/2018
ms.keywords: IEnumEventObject interface [COM+],Next method, IEnumEventObject.Next, IEnumEventObject::Next, Next, Next method [COM+], Next method [COM+],IEnumEventObject interface, _cos_ienumeventobject_next, cos.ienumeventobject_next, eventsys/IEnumEventObject::Next
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
 - IEnumEventObject::Next
 - eventsys/IEnumEventObject::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Eventsys.h
api_name:
 - IEnumEventObject.Next
---

# IEnumEventObject::Next


## -description

Retrieves the specified number of items in the enumeration sequence.

## -parameters

### -param cReqElem [in]

The number of elements being requested. If there are fewer than the requested number of elements left in the sequence, this method obtains the remaining elements.

### -param ppInterface [out]

The address to a pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the first object obtained. This parameter cannot be <b>NULL</b>.

### -param cRetElem [out]

The number of elements actually obtained. This parameter cannot be <b>NULL</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_POINTER, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
All elements requested were obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Not all elements requested were obtained. The number of elements obtained was written to <i>pcRetElem</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ienumeventobject">IEnumEventObject</a>
