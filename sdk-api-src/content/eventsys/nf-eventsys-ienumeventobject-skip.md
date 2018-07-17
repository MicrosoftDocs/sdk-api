---
UID: NF:eventsys.IEnumEventObject.Skip
title: IEnumEventObject::Skip
author: windows-sdk-content
description: Skips over the specified number of items in the enumeration sequence.
old-location: cos\ienumeventobject_skip.htm
old-project: cossdk
ms.assetid: 7c830d29-8e66-4139-9445-d83dc7f7004f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IEnumEventObject interface [COM+],Skip method, IEnumEventObject.Skip, IEnumEventObject::Skip, Skip, Skip method [COM+], Skip method [COM+],IEnumEventObject interface, _cos_ienumeventobject_skip, cos.ienumeventobject_skip, eventsys/IEnumEventObject::Skip
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
 - eventsys.h
api_name:
 - IEnumEventObject.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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




<a href="https://msdn.microsoft.com/a42d0791-28d0-4d83-b94d-ff2f8ef9a614">IEnumEventObject</a>
 

 

