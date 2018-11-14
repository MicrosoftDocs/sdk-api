---
UID: NN:winsync.IEnumClockVector
title: IEnumClockVector
author: windows-sdk-content
description: Enumerates the clock vector elements that are stored in a clock vector.
old-location: winsync\ienumclockvector.htm
tech.root: winsync
ms.assetid: cf191502-dc51-44a7-a82f-a0e38537574f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IEnumClockVector, IEnumClockVector interface [Windows Sync], IEnumClockVector interface [Windows Sync],described, winsync.ienumclockvector, winsync/IEnumClockVector
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - winsync.h
api_name:
 - IEnumClockVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumClockVector interface


## -description


Enumerates the clock vector elements that are stored in a clock vector.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumClockVector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumClockVector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumClockVector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17e8704f-15fe-4d08-9e83-fd7b9a064569">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40aa741a-b536-4a8b-9f97-b7b599e49aef">Next</a>
</td>
<td align="left" width="63%">
Returns the next elements in the clock vector, if they are available.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf61db66-c621-486a-a70a-5d24d3cf74da">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the clock vector.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76f76535-7f1f-431b-9b35-7bbb0d645dcd">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of clock vector elements.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

