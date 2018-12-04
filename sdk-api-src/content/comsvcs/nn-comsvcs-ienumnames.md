---
UID: NN:comsvcs.IEnumNames
title: IEnumNames
author: windows-sdk-content
description: Enumerates names.
old-location: cos\ienumnames.htm
tech.root: cossdk
ms.assetid: 9f70b554-3cdd-4a4b-b180-c6de6182a46a
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IEnumNames, IEnumNames interface [COM+], IEnumNames interface [COM+],described, _cos_IEnumNames, comsvcs/IEnumNames, cos.ienumnames
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ComSvcs.h
api_name:
 - IEnumNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumNames interface


## -description


Enumerates names.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNames</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumNames</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumNames</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea57be73-076a-445d-9b0d-4a1041befa2d">Clone</a>
</td>
<td align="left" width="63%">
Creates an enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa20453f-f170-442d-a927-6872ca75dbed">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7b7e703-f5d5-430f-8fa6-c26a236eab88">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e45da100-688a-421e-a8cd-19fede5aac83">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/95a5cfda-7587-496e-ba16-0dd2e8a4db32">IContextProperties</a>
 

 

