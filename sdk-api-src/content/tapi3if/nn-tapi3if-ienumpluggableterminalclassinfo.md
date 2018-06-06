---
UID: NN:tapi3if.IEnumPluggableTerminalClassInfo
title: IEnumPluggableTerminalClassInfo
author: windows-sdk-content
description: The IEnumPluggableTerminalClassInfo interface provides COM-standard enumeration methods for the ITPluggableTerminalClassInfo interface. The ITTerminalSupport2::EnumeratePluggableTerminalClasses method returns a pointer to IEnumPluggableTerminalClassInfo.
old-location: tapi3\ienumpluggableterminalclassinfo.htm
old-project: Tapi
ms.assetid: 72c0db41-8391-4923-8961-6aefce9886c4
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IEnumPluggableTerminalClassInfo, IEnumPluggableTerminalClassInfo interface [TAPI 2.2], IEnumPluggableTerminalClassInfo interface [TAPI 2.2],described, _tapi3_ienumpluggableterminalclassinfo, tapi3.ienumpluggableterminalclassinfo, tapi3if/IEnumPluggableTerminalClassInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumPluggableTerminalClassInfo
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumPluggableTerminalClassInfo interface


## -description


The 
<b>IEnumPluggableTerminalClassInfo</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/0f7190c4-c696-4749-82f2-20fdbc8651f4">ITPluggableTerminalClassInfo</a> interface. The 
<a href="https://msdn.microsoft.com/e8a10b1b-b08e-49b2-bfc6-9f8f4dbc1248">ITTerminalSupport2::EnumeratePluggableTerminalClasses</a> method returns a pointer to 
<b>IEnumPluggableTerminalClassInfo</b>.

The 
<b>IEnumPluggableTerminalClassInfo</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPluggableTerminalClassInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumPluggableTerminalClassInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumPluggableTerminalClassInfo</b> interface has these methods.
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




<a href="https://msdn.microsoft.com/0f7190c4-c696-4749-82f2-20fdbc8651f4">ITPluggableTerminalClassInfo</a>



<a href="https://msdn.microsoft.com/e8a10b1b-b08e-49b2-bfc6-9f8f4dbc1248">ITTerminalSupport2::EnumeratePluggableTerminalClasses</a>



<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">Terminal Class</a>
 

 

