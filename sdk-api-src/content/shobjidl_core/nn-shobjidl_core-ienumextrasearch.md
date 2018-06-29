---
UID: NN:shobjidl_core.IEnumExtraSearch
title: IEnumExtraSearch
author: windows-sdk-content
description: A standard OLE enumerator used by a client to determine the available search objects for a folder.
old-location: shell\IEnumExtraSearch.htm
old-project: shell
ms.assetid: 63b71cd2-483b-482f-b3f4-6d5c937e7708
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IEnumExtraSearch, IEnumExtraSearch interface [Windows Shell], IEnumExtraSearch interface [Windows Shell],described, _win32_IEnumExtraSearch, shell.IEnumExtraSearch, shobjidl_core/IEnumExtraSearch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEnumExtraSearch
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IEnumExtraSearch interface


## -description


A standard OLE enumerator used by a client to determine the available search objects for a folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumExtraSearch</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumExtraSearch</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumExtraSearch</b> interface has these methods.
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
Used to request a duplicate of the enumerator object to preserve its current state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Used to request information on one or more search objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Used to reset the enumeration index to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skip a specified number of objects.

</td>
</tr>
</table> 


## -remarks



Implement <b>IEnumExtraSearch</b> if your namespace extension supports one or more search objects.

You do not call this interface directly. An <b>IEnumExtraSearch</b> interface is requested by a client only after it has determined that the <a href="https://msdn.microsoft.com/9b008034-3576-429e-b67c-e2222592ca46">IShellFolder2</a> interface is exposed. Clients retrieve a pointer to this interface by calling <a href="https://msdn.microsoft.com/ed7b0e3c-f679-491b-98a2-542fcf5d2077">IShellFolder2::EnumSearches</a>.

<b>IEnumExtraSearch</b> implements <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and the standard OLE enumeration methods.



