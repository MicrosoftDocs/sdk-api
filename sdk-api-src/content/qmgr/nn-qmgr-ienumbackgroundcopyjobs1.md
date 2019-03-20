---
UID: NN:qmgr.IEnumBackgroundCopyJobs1
title: IEnumBackgroundCopyJobs1 (qmgr.h)
author: windows-sdk-content
description: Use the IEnumBackgroundCopyJobs1 interface to enumerate the list of jobs in a group. To get an IEnumBackgroundCopyJobs1 interface pointer, call the IBackgroundCopyGroup::EnumJobs method.
old-location: bits\ienumbackgroundcopyjobs1.htm
tech.root: Bits
ms.assetid: 93feac90-8eb8-49d8-9841-d78a2645fbcb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumBackgroundCopyJobs1, IEnumBackgroundCopyJobs1 interface [BITS], IEnumBackgroundCopyJobs1 interface [BITS],described, bits.ienumbackgroundcopyjobs1, qmgr/IEnumBackgroundCopyJobs1
ms.topic: interface
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IEnumBackgroundCopyJobs1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumBackgroundCopyJobs1 interface


## -description


<p class="CCE_Message">[<b>IEnumBackgroundCopyJobs1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>IEnumBackgroundCopyJobs1</b> interface to enumerate the list of jobs in a group. To get an <b>IEnumBackgroundCopyJobs1</b> interface pointer, call the <a href="https://msdn.microsoft.com/40e4412e-60d5-4e08-85b9-1e92f5222e71">IBackgroundCopyGroup::EnumJobs</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumBackgroundCopyJobs1</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumBackgroundCopyJobs1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumBackgroundCopyJobs1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c26bec86-1cff-44bb-aa0c-c48b076ff993">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3deaf2fd-84a0-49f8-8a7d-91a39701683a">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15dcc2e1-7fdf-4c4a-a24b-2cad49bda7fc">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44f29932-8bcd-4c46-b0b5-c949f3061015">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b388530c-688a-46a9-ae23-370f902b870e">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table> 

