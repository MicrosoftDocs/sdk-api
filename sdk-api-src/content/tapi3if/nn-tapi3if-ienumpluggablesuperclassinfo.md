---
UID: NN:tapi3if.IEnumPluggableSuperclassInfo
title: IEnumPluggableSuperclassInfo
author: windows-driver-content
description: The IEnumPluggableSuperclassInfo interface provides COM-standard enumeration methods for the ITPluggableTerminalSuperclassInfo interface. The ITTerminalSupport2::EnumeratePluggableSuperclasses method returns a pointer to IEnumPluggableSuperclassInfo.
old-location: tapi3\ienumpluggablesuperclassinfo.htm
old-project: Tapi
ms.assetid: 80b84976-4256-47d2-a965-3ebe89a3821a
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IEnumPluggableSuperclassInfo, IEnumPluggableSuperclassInfo interface [TAPI 2.2], IEnumPluggableSuperclassInfo interface [TAPI 2.2],described, _tapi3_ienumpluggablesuperclassinfo, tapi3.ienumpluggablesuperclassinfo, tapi3if/IEnumPluggableSuperclassInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tapi3if.h
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	IEnumPluggableSuperclassInfo
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumPluggableSuperclassInfo interface


## -description


The 
<b>IEnumPluggableSuperclassInfo</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a> interface. The 
<a href="https://msdn.microsoft.com/5f1e8490-1b26-45e6-9f9a-e7ddcc840e90">ITTerminalSupport2::EnumeratePluggableSuperclasses</a> method returns a pointer to 
<b>IEnumPluggableSuperclassInfo</b>.

The 
<b>IEnumPluggableSuperclassInfo</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPluggableSuperclassInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumPluggableSuperclassInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumPluggableSuperclassInfo</b> interface has these methods.
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
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

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
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a>



<a href="https://msdn.microsoft.com/5f1e8490-1b26-45e6-9f9a-e7ddcc840e90">ITTerminalSupport2::EnumeratePluggableSuperclasses</a>
 

 

