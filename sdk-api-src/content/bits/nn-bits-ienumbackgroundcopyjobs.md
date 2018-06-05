---
UID: NN:bits.IEnumBackgroundCopyJobs
title: IEnumBackgroundCopyJobs
author: windows-sdk-content
description: Use the IEnumBackgroundCopyJobs interface to enumerate the list of jobs in the transfer queue. To get an IEnumBackgroundCopyJobs interface pointer, call the IBackgroundCopyManager::EnumJobs method.
old-location: bits\ienumbackgroundcopyjobs.htm
old-project: Bits
ms.assetid: 21ff88da-9fae-478f-bcba-488ed7a89608
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IEnumBackgroundCopyJobs, IEnumBackgroundCopyJobs interface [BITS], IEnumBackgroundCopyJobs interface [BITS],described, _drz_ienumbackgroundcopyjobs, bits.ienumbackgroundcopyjobs, bits/IEnumBackgroundCopyJobs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IEnumBackgroundCopyJobs
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IEnumBackgroundCopyJobs interface


## -description


Use the 
<b>IEnumBackgroundCopyJobs</b> interface to enumerate the list of jobs in the transfer queue. To get an 
<b>IEnumBackgroundCopyJobs</b> interface pointer, call the 
<a href="https://msdn.microsoft.com/e8b73060-dff9-4ab3-8009-d2b41502fc1a">IBackgroundCopyManager::EnumJobs</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumBackgroundCopyJobs</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumBackgroundCopyJobs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumBackgroundCopyJobs</b> interface has these methods.
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

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
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e8b73060-dff9-4ab3-8009-d2b41502fc1a">IBackgroundCopyManager::EnumJobs</a>



<a href="https://msdn.microsoft.com/831998ba-601c-43c4-ba27-faff741f8eb4">IEnumBackgroundCopyFiles</a>
 

 

