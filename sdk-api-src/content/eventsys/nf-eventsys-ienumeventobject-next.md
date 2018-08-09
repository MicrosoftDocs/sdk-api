---
UID: NF:eventsys.IEnumEventObject.Next
title: IEnumEventObject::Next
author: windows-sdk-content
description: Retrieves the specified number of items in the enumeration sequence.
old-location: cos\ienumeventobject_next.htm
old-project: cossdk
ms.assetid: c9dab0b5-dbbb-4330-afd2-e13e708d708f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumEventObject interface [COM+],Next method, IEnumEventObject.Next, IEnumEventObject::Next, Next, Next method [COM+], Next method [COM+],IEnumEventObject interface, _cos_ienumeventobject_next, cos.ienumeventobject_next, eventsys/IEnumEventObject::Next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: EOC_ChangeType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Eventsys.h
api_name:
 - IEnumEventObject.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnumEventObject::Next


## -description


Retrieves the specified number of items in the enumeration sequence.


## -parameters




### -param cReqElem [in]

The number of elements being requested. If there are fewer than the requested number of elements left in the sequence, this method obtains the remaining elements.


### -param ppInterface [out]

The address to a pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the first object obtained. This parameter cannot be <b>NULL</b>.


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




<a href="https://msdn.microsoft.com/a42d0791-28d0-4d83-b94d-ff2f8ef9a614">IEnumEventObject</a>
 

 

