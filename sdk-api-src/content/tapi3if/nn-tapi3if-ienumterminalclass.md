---
UID: NN:tapi3if.IEnumTerminalClass
title: IEnumTerminalClass
author: windows-driver-content
description: The IEnumTerminalClass interface provides COM-standard enumeration methods to discover and use the dynamic terminal classes that are available. The ITTerminalSupport::EnumerateDynamicTerminalClasses method returns a pointer to this interface.
old-location: tapi3\ienumterminalclass.htm
old-project: Tapi
ms.assetid: 1da0a82a-fde4-440c-ac6c-e9b85a7ec3fe
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IEnumTerminalClass, IEnumTerminalClass interface [TAPI 2.2], IEnumTerminalClass interface [TAPI 2.2],described, _tapi3_ienumterminalclass, tapi3.ienumterminalclass, tapi3if/IEnumTerminalClass
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
-	IEnumTerminalClass
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumTerminalClass interface


## -description


The 
<b>IEnumTerminalClass</b> interface provides COM-standard enumeration methods to discover and use the dynamic terminal classes that are available. The 
<a href="https://msdn.microsoft.com/1dcb9163-306b-42fc-afb4-41b33d7e2d40">ITTerminalSupport::EnumerateDynamicTerminalClasses</a> method returns a pointer to this interface.

The 
<b>IEnumTerminalClass</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTerminalClass</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTerminalClass</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTerminalClass</b> interface has these methods.
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
Resets to the beginning of the enumeration sequence.

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




<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

