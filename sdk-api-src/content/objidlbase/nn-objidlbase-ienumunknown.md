---
UID: NN:objidlbase.IEnumUnknown
title: IEnumUnknown
author: windows-driver-content
description: Enumerates objects with the IUnknown interface. It can be used to enumerate through the objects in a component containing multiple objects.
old-location: com\ienumunknown.htm
old-project: com
ms.assetid: 5aaed96f-39c1-4201-80d0-a2a8a177b65e
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IEnumUnknown, IEnumUnknown interface [COM], IEnumUnknown interface [COM], described, _com_ienumunknown, com.ienumunknown, objidlbase/IEnumUnknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IEnumUnknown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumUnknown interface


## -description


Enumerates objects with the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. It can be used to enumerate through the objects in a component containing multiple objects. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumUnknown</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IEnumUnknown</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumUnknown</b> interface has these methods.
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
Creates a new enumerator that contains the same enumeration state as the current one.

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




<a href="https://msdn.microsoft.com/98549309-8ac8-4391-92ab-8a62269ff579">IOleContainer</a>
 

 

