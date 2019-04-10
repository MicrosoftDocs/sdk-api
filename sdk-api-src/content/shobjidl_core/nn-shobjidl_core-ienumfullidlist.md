---
UID: NN:shobjidl_core.IEnumFullIDList
title: IEnumFullIDList (shobjidl_core.h)
author: windows-sdk-content
description: Exposes a standard set of methods that enumerate the pointers to item identifier lists (PIDLs) of the items in a Shell folder.
old-location: shell\IEnumFullIDList.htm
tech.root: shell
ms.assetid: 1350e914-7935-42dd-b1b0-e447589dfb12
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumFullIDList, IEnumFullIDList interface [Windows Shell], IEnumFullIDList interface [Windows Shell],described, _shell_IEnumFullIDList, shell.IEnumFullIDList, shobjidl_core/IEnumFullIDList
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IEnumFullIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumFullIDList interface


## -description


Exposes a standard set of methods that enumerate the pointers to item identifier lists (PIDLs) of the items in a Shell folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumFullIDList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumFullIDList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumFullIDList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23345978-6178-4f6d-8757-d5fd95199067">Clone</a>
</td>
<td align="left" width="63%">
Creates a new item enumeration object with the same contents and state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/023f8935-0382-404e-b1bf-737824cf0f34">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of IDLIST_ABSOLUTE items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9682cfc4-544b-43bd-bd57-edbce50dce75">Reset</a>
</td>
<td align="left" width="63%">
Returns the enumerator to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f47bdab1-57be-4f40-a142-ad5edcf6fbfd">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of IDLIST_ABSOLUTE  items.

</td>
</tr>
</table> 

