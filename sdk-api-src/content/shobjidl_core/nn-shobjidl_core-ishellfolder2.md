---
UID: NN:shobjidl_core.IShellFolder2
title: IShellFolder2 (shobjidl_core.h)
description: Extends the capabilities of IShellFolder. Its methods provide a variety of information about the contents of a Shell folder.helpviewer_keywords: ["IShellFolder2","IShellFolder2 interface [Windows Shell]","IShellFolder2 interface [Windows Shell]","described","_win32_IShellFolder2","shell.IShellFolder2","shobjidl_core/IShellFolder2"]
old-location: shell\IShellFolder2.htm
tech.root: shell
ms.assetid: 9b008034-3576-429e-b67c-e2222592ca46
ms.date: 12/05/2018
ms.keywords: IShellFolder2, IShellFolder2 interface [Windows Shell], IShellFolder2 interface [Windows Shell],described, _win32_IShellFolder2, shell.IShellFolder2, shobjidl_core/IShellFolder2
f1_keywords:
- shobjidl_core/IShellFolder2
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellFolder2 interface


## -description


Extends the capabilities of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>. Its methods provide a variety of information about the contents of a Shell folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolder2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>. <b>IShellFolder2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-enumsearches">EnumSearches</a>
</td>
<td align="left" width="63%">
Requests a pointer to an interface that allows a client to enumerate the available search objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumn">GetDefaultColumn</a>
</td>
<td align="left" width="63%">
Gets the default sorting and display columns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate">GetDefaultColumnState</a>
</td>
<td align="left" width="63%">
Gets the default state for a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultsearchguid">GetDefaultSearchGUID</a>
</td>
<td align="left" width="63%">
Returns the globally unique identifier (GUID) of the default search object for the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex">GetDetailsEx</a>
</td>
<td align="left" width="63%">
Gets detailed information, identified by a property set identifier (FMTID) and a PID, on an item in a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof">GetDetailsOf</a>
</td>
<td align="left" width="63%">
Gets detailed information, identified by a column index, on an item in a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-mapcolumntoscid">MapColumnToSCID</a>
</td>
<td align="left" width="63%">
Converts a column to the appropriate property set ID (FMTID) and property ID (PID).

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IShellFolder2</b> if your namespace extension provides services to clients beyond those in <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Call <b>IShellFolder2</b> when you need detailed information on items contained by a Shell folder. This interface supersedes <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails">IShellDetails</a>.



