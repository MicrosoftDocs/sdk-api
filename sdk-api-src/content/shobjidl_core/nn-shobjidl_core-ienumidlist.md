---
UID: NN:shobjidl_core.IEnumIDList
title: IEnumIDList
author: windows-sdk-content
description: Exposes a standard set of methods used to enumerate the pointers to item identifier lists (PIDLs) of the items in a Shell folder.
old-location: shell\IEnumIDList.htm
tech.root: shell
ms.assetid: b6f139d3-c54c-4350-9d8b-cd534909a488
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IEnumIDList, IEnumIDList interface [Windows Shell], IEnumIDList interface [Windows Shell],described, _win32_IEnumIDList, shell.IEnumIDList, shobjidl_core/IEnumIDList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEnumIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumIDList interface


## -description


Exposes a standard set of methods used to enumerate the pointers to item identifier lists (PIDLs) of the items in a Shell folder. When a folder's <a href="https://msdn.microsoft.com/248bec8b-0bf4-47d5-adb3-31a685a2c359">IShellFolder::EnumObjects</a> method is called, it creates an enumeration object and passes a pointer to the object's <b>IEnumIDList</b> interface back to the calling application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumIDList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumIDList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumIDList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0118153-25ea-42d6-90bf-b85ffd99b74b">Clone</a>
</td>
<td align="left" width="63%">
Creates a new item enumeration object with the same contents and state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b2cd7a3-687c-4a51-b9af-a01576463f0b">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of item identifiers in the enumeration sequence and advances the current position by the number of items retrieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2ce1947-ca8b-4f0c-a94a-d1aba42b105d">Reset</a>
</td>
<td align="left" width="63%">
Returns to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed9d5774-7b2f-4a25-88f9-70d72919ff60">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -remarks



All Shell folder objects must be able to respond to a call to their <a href="https://msdn.microsoft.com/248bec8b-0bf4-47d5-adb3-31a685a2c359">IShellFolder::EnumObjects</a> method by creating an enumeration object that exports <b>IEnumIDList</b>. The Shell, in particular, uses these objects to enumerate the items in a folder.

Use this interface to enumerate the contents of a Shell folder object. Call the folder's <a href="https://msdn.microsoft.com/248bec8b-0bf4-47d5-adb3-31a685a2c359">IShellFolder::EnumObjects</a> method and use the returned <b>IEnumIDList</b> pointer to enumerate the PIDLs of the items in the folder.



