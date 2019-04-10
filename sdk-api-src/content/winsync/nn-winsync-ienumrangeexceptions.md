---
UID: NN:winsync.IEnumRangeExceptions
title: IEnumRangeExceptions (winsync.h)
author: windows-sdk-content
description: Enumerates range exceptions that are stored in a knowledge object.
old-location: winsync\ienumrangeexceptions.htm
tech.root: winsync
ms.assetid: 1b2724a3-2f5f-4f30-8cf5-e31f16d4cd14
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumRangeExceptions, IEnumRangeExceptions interface [Windows Sync], IEnumRangeExceptions interface [Windows Sync],described, winsync.ienumrangeexceptions, winsync/IEnumRangeExceptions
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
 - IEnumRangeExceptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumRangeExceptions interface


## -description


Enumerates range exceptions that are stored in a knowledge object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumRangeExceptions</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumRangeExceptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumRangeExceptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9ba5d49-754f-4eb0-972b-67e9a6a41994">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ca472d7-4e97-4998-b883-05329dfdb27a">Next</a>
</td>
<td align="left" width="63%">
Returns the next elements in the range exception set, if they are available.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4056703-8218-4b0b-9ed6-4c1584f0b751">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the range exception set.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61907858-4089-4c12-865c-623a43132be3">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of range exceptions.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

