---
UID: NN:winsync.IEnumSingleItemExceptions
title: IEnumSingleItemExceptions
author: windows-sdk-content
description: Enumerates single-item exceptions that are stored in a knowledge object.
old-location: winsync\ienumsingleitemexceptions.htm
old-project: winsync
ms.assetid: fed8a258-bc23-454b-9d8a-e3873481b33b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IEnumSingleItemExceptions, IEnumSingleItemExceptions interface [Windows Sync], IEnumSingleItemExceptions interface [Windows Sync],described, winsync.ienumsingleitemexceptions, winsync/IEnumSingleItemExceptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IEnumSingleItemExceptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IEnumSingleItemExceptions interface


## -description


Enumerates single-item exceptions that are stored in a knowledge object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSingleItemExceptions</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSingleItemExceptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSingleItemExceptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89a02939-e761-450e-9479-29e19a872da6">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9605eaa-2b68-4bc6-9dcf-c2bebc4e6f1b">Next</a>
</td>
<td align="left" width="63%">
Returns the next elements in the single-item exception set, if they are available.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbd65da9-d5bb-463e-aec6-763be41079ce">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the single-item exception set.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80e3bb55-b467-4fa4-bb3e-70233e5b0265">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of single item exceptions.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

