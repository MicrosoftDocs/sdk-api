---
UID: NN:eventsys.IEnumEventObject
title: IEnumEventObject
author: windows-driver-content
description: Enumerates the event objects that are registered in the COM+ events store.
old-location: cos\ienumeventobject.htm
old-project: cossdk
ms.assetid: a42d0791-28d0-4d83-b94d-ff2f8ef9a614
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IEnumEventObject, IEnumEventObject interface [COM+], IEnumEventObject interface [COM+],described, _cos_ienumeventobject, cos.ienumeventobject, eventsys/IEnumEventObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Eventsys.h
api_name:
-	IEnumEventObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnumEventObject interface


## -description


Enumerates the event objects that are registered in the COM+ events store.

Similar functionality is available through <a href="https://msdn.microsoft.com/7bb00b80-a48f-49c8-983d-9ff0ea424e4d">IEventObjectCollection</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumEventObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumEventObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumEventObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">

Creates an enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">

Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">

Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">

Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7bb00b80-a48f-49c8-983d-9ff0ea424e4d">IEventObjectCollection</a>
 

 

