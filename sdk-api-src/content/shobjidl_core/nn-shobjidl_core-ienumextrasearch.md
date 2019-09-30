---
UID: NN:shobjidl_core.IEnumExtraSearch
title: IEnumExtraSearch (shobjidl_core.h)
author: windows-sdk-content
description: A standard OLE enumerator used by a client to determine the available search objects for a folder.
old-location: shell\IEnumExtraSearch.htm
tech.root: shell
ms.assetid: 63b71cd2-483b-482f-b3f4-6d5c937e7708
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumExtraSearch, IEnumExtraSearch interface [Windows Shell], IEnumExtraSearch interface [Windows Shell],described, _win32_IEnumExtraSearch, shell.IEnumExtraSearch, shobjidl_core/IEnumExtraSearch
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IEnumExtraSearch"
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEnumExtraSearch
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumExtraSearch interface


## -description


A standard OLE enumerator used by a client to determine the available search objects for a folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumExtraSearch</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumExtraSearch</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumextrasearch-clone">Clone</a>
</td>
<td align="left" width="63%">
Used to request a duplicate of the enumerator object to preserve its current state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumextrasearch-next">Next</a>
</td>
<td align="left" width="63%">
Used to request information on one or more search objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumextrasearch-reset">Reset</a>
</td>
<td align="left" width="63%">
Used to reset the enumeration index to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumextrasearch-skip">Skip</a>
</td>
<td align="left" width="63%">
Skip a specified number of objects.

</td>
</tr>
</table> 


## -remarks



Implement <b>IEnumExtraSearch</b> if your namespace extension supports one or more search objects.

You do not call this interface directly. An <b>IEnumExtraSearch</b> interface is requested by a client only after it has determined that the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a> interface is exposed. Clients retrieve a pointer to this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-enumsearches">IShellFolder2::EnumSearches</a>.

<b>IEnumExtraSearch</b> implements <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and the standard OLE enumeration methods.



