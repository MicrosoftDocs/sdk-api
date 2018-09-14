---
UID: NF:eventsys.IEnumEventObject.Reset
title: IEnumEventObject::Reset
author: windows-sdk-content
description: Resets the enumeration sequence to the beginning.
old-location: cos\ienumeventobject_reset.htm
tech.root: cossdk
ms.assetid: 9a92c9de-e259-4b62-8f74-dff3f9947d1a
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IEnumEventObject interface [COM+],Reset method, IEnumEventObject.Reset, IEnumEventObject::Reset, Reset, Reset method [COM+], Reset method [COM+],IEnumEventObject interface, _cos_ienumeventobject_reset, cos.ienumeventobject_reset, eventsys/IEnumEventObject::Reset
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Eventsys.h
api_name:
 - IEnumEventObject.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumEventObject::Reset


## -description


Resets the enumeration sequence to the beginning.


## -parameters






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
The enumeration sequence was reset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The enumeration sequence was reset, but there are no items in the enumerator.

</td>
</tr>
</table>
 




## -remarks



You can use the S_FALSE return value as an optimization to detect an empty enumeration.

A call to this method, resetting the sequence, does not guarantee that the same set of objects will be enumerated after the reset, because the collection may have changed.




## -see-also




<a href="https://msdn.microsoft.com/a42d0791-28d0-4d83-b94d-ff2f8ef9a614">IEnumEventObject</a>
 

 

