---
UID: NN:tapi3if.IEnumTerminal
title: IEnumTerminal
author: windows-sdk-content
description: The IEnumTerminal interface provides COM-standard enumeration methods for the ITTerminal interface.
old-location: tapi3\ienumterminal.htm
old-project: tapi
ms.assetid: a364e466-1d10-402f-935d-ff2713522fed
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: IEnumTerminal, IEnumTerminal interface [TAPI 2.2], IEnumTerminal interface [TAPI 2.2],described, _tapi3_ienumterminal, tapi3.ienumterminal, tapi3if/IEnumTerminal
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
 - IEnumTerminal
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumTerminal interface


## -description


The 
<b>IEnumTerminal</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface. The following methods return a pointer to 
<b>IEnumTerminal</b>:<dl>
<dd>
<a href="https://msdn.microsoft.com/c57af2a9-a2ec-45ba-9e10-7b5f41bdeb00">ITStream::EnumerateTerminals</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/bf5e1f7f-3820-433e-b71f-53798c202593">ITSubStream::EnumerateTerminals</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/91fea706-9792-40e1-b812-f7578bc7968b">ITTerminalSupport::EnumerateStaticTerminals</a>
</dd>
</dl>


The 
<b>IEnumTerminal</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTerminal</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTerminal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTerminal</b> interface has these methods.
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
 

 

