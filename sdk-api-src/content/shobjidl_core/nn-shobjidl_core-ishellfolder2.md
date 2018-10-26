---
UID: NN:shobjidl_core.IShellFolder2
title: IShellFolder2
author: windows-sdk-content
description: Extends the capabilities of IShellFolder. Its methods provide a variety of information about the contents of a Shell folder.
old-location: shell\IShellFolder2.htm
tech.root: shell
ms.assetid: 9b008034-3576-429e-b67c-e2222592ca46
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IShellFolder2, IShellFolder2 interface [Windows Shell], IShellFolder2 interface [Windows Shell],described, _win32_IShellFolder2, shell.IShellFolder2, shobjidl_core/IShellFolder2
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later); Netshell.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
 - netshell.dll
api_name:
 - IShellFolder2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolder2 interface


## -description


Extends the capabilities of <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>. Its methods provide a variety of information about the contents of a Shell folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolder2</b> interface inherits from <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>. <b>IShellFolder2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellFolder2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed7b0e3c-f679-491b-98a2-542fcf5d2077">EnumSearches</a>
</td>
<td align="left" width="63%">
Requests a pointer to an interface that allows a client to enumerate the available search objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d1a1273-be67-4bb3-b549-8adacea0cb5f">GetDefaultColumn</a>
</td>
<td align="left" width="63%">
Gets the default sorting and display columns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f55acbf-1e15-42c3-a610-c5742e74883d">GetDefaultColumnState</a>
</td>
<td align="left" width="63%">
Gets the default state for a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20acd646-6cb7-420e-84b3-2f9b385a349c">GetDefaultSearchGUID</a>
</td>
<td align="left" width="63%">
Returns the globally unique identifier (GUID) of the default search object for the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f006828c-980d-4e36-be68-3b3c238cd884">GetDetailsEx</a>
</td>
<td align="left" width="63%">
Gets detailed information, identified by a property set identifier (FMTID) and a PID, on an item in a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd9e8b6c-ed70-455e-8316-ac0868493802">GetDetailsOf</a>
</td>
<td align="left" width="63%">
Gets detailed information, identified by a column index, on an item in a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bd1f9a1-379b-4488-87d3-c7c7dc47c4d1">MapColumnToSCID</a>
</td>
<td align="left" width="63%">
Converts a column to the appropriate property set ID (FMTID) and property ID (PID).

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IShellFolder2</b> if your namespace extension provides services to clients beyond those in <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Call <b>IShellFolder2</b> when you need detailed information on items contained by a Shell folder. This interface supersedes <a href="https://msdn.microsoft.com/c31409fd-9350-46bb-a8a0-85d5958c6e49">IShellDetails</a>.



