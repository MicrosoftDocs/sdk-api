---
UID: NN:shobjidl_core.IEnumFullIDList
title: IEnumFullIDList (shobjidl_core.h)
description: Exposes a standard set of methods that enumerate the pointers to item identifier lists (PIDLs) of the items in a Shell folder.helpviewer_keywords: ["IEnumFullIDList","IEnumFullIDList interface [Windows Shell]","IEnumFullIDList interface [Windows Shell]","described","_shell_IEnumFullIDList","shell.IEnumFullIDList","shobjidl_core/IEnumFullIDList"]
old-location: shell\IEnumFullIDList.htm
tech.root: shell
ms.assetid: 1350e914-7935-42dd-b1b0-e447589dfb12
ms.date: 12/05/2018
ms.keywords: IEnumFullIDList, IEnumFullIDList interface [Windows Shell], IEnumFullIDList interface [Windows Shell],described, _shell_IEnumFullIDList, shell.IEnumFullIDList, shobjidl_core/IEnumFullIDList
f1_keywords:
- shobjidl_core/IEnumFullIDList
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumFullIDList interface


## -description


Exposes a standard set of methods that enumerate the pointers to item identifier lists (PIDLs) of the items in a Shell folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumFullIDList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumFullIDList</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumfullidlist-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new item enumeration object with the same contents and state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumfullidlist-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of IDLIST_ABSOLUTE items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumfullidlist-reset">Reset</a>
</td>
<td align="left" width="63%">
Returns the enumerator to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumfullidlist-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of IDLIST_ABSOLUTE  items.

</td>
</tr>
</table> 

