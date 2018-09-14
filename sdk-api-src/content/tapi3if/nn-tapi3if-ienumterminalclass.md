---
UID: NN:tapi3if.IEnumTerminalClass
title: IEnumTerminalClass
author: windows-sdk-content
description: The IEnumTerminalClass interface provides COM-standard enumeration methods to discover and use the dynamic terminal classes that are available. The ITTerminalSupport::EnumerateDynamicTerminalClasses method returns a pointer to this interface.
old-location: tapi3\ienumterminalclass.htm
tech.root: TAPI
ms.assetid: 1da0a82a-fde4-440c-ac6c-e9b85a7ec3fe
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IEnumTerminalClass, IEnumTerminalClass interface [TAPI 2.2], IEnumTerminalClass interface [TAPI 2.2],described, _tapi3_ienumterminalclass, tapi3.ienumterminalclass, tapi3if/IEnumTerminalClass
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumTerminalClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/60b4005f-25a8-4544-b2c9-0c12c3f93618">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67ed4017-9cd2-4694-9853-c07bd4f81e0a">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd61649e-d684-4774-bd23-91990e20729a">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5aebbc0d-212e-4789-bb8e-d180589235ec">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

