---
UID: NN:winsync.IEnumChangeUnitExceptions
title: IEnumChangeUnitExceptions
author: windows-sdk-content
description: Enumerates change unit exceptions that are stored in a knowledge object.
old-location: winsync\ienumchangeunitexceptions.htm
tech.root: winsync
ms.assetid: 40b2977e-f3ae-4ad2-89ed-aacf32b1171e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumChangeUnitExceptions, IEnumChangeUnitExceptions interface [Windows Sync], IEnumChangeUnitExceptions interface [Windows Sync],described, winsync.ienumchangeunitexceptions, winsync/IEnumChangeUnitExceptions
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
 - IEnumChangeUnitExceptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumChangeUnitExceptions interface


## -description


Enumerates change unit exceptions that are stored in a knowledge object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumChangeUnitExceptions</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumChangeUnitExceptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumChangeUnitExceptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8039d175-f0d9-44af-9571-e4f97b6cd43f">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97bf473d-4e63-4192-a5d8-b802d5887a55">Next</a>
</td>
<td align="left" width="63%">
Returns the next elements in the change unit exception set, if they are available.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c9a98e2-c976-42cb-ada3-ee33c11adae8">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the change unit exception set.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71e325cc-b686-4db5-988f-abf08af48d1c">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of change unit exceptions.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

