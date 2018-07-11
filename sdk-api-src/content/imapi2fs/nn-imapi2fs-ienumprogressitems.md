---
UID: NN:imapi2fs.IEnumProgressItems
title: IEnumProgressItems
author: windows-sdk-content
description: Use this interface to enumerate a collection of progress items.
old-location: imapi\ienumprogressitems.htm
old-project: imapi
ms.assetid: c4238fbe-762a-492f-9eb5-d927e64436e1
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: IEnumProgressItems, IEnumProgressItems interface [IMAPI], IEnumProgressItems interface [IMAPI],described, imapi.ienumprogressitems, imapi2fs/IEnumProgressItems
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PlatformId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IEnumProgressItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IEnumProgressItems interface


## -description


Use this interface to enumerate a collection of progress items.

To get this interface, call the <a href="https://msdn.microsoft.com/746b05b7-ddba-458c-bc9b-4913da5fa8b5">IProgressItems::get_EnumProgressItems</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumProgressItems</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumProgressItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumProgressItems</b> interface has these methods.
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
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5f85ca3-1bad-49fd-9e67-d41135cd837d">RemoteNext</a>
</td>
<td align="left" width="63%">
Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence.

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


## -remarks



This is a <b>EnumProgressItems</b> object in script.




## -see-also




<a href="https://msdn.microsoft.com/b6ba9226-655e-4eac-ad43-2b5a8e90039f">IProgressItem</a>



<a href="https://msdn.microsoft.com/40c28e67-8ff3-4330-90a1-7ebccb0023ad">IProgressItems</a>
 

 

