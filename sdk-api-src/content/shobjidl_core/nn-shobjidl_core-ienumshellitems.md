---
UID: NN:shobjidl_core.IEnumShellItems
title: IEnumShellItems (shobjidl_core.h)
description: Exposes enumeration of IShellItem interfaces. This interface is typically obtained by calling the IEnumShellItems method.
helpviewer_keywords: ["IEnumShellItems","IEnumShellItems interface [Windows Shell]","IEnumShellItems interface [Windows Shell]","described","_shell_IEnumShellItems","shell.IEnumShellItems","shobjidl_core/IEnumShellItems"]
old-location: shell\IEnumShellItems.htm
tech.root: shell
ms.assetid: 07aed597-359f-4f4b-9edf-168c15bdc58e
ms.date: 12/05/2018
ms.keywords: IEnumShellItems, IEnumShellItems interface [Windows Shell], IEnumShellItems interface [Windows Shell],described, _shell_IEnumShellItems, shell.IEnumShellItems, shobjidl_core/IEnumShellItems
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumShellItems
 - shobjidl_core/IEnumShellItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IEnumShellItems
---

# IEnumShellItems interface


## -description

Exposes enumeration of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interfaces. This interface is typically obtained by calling the <b>IEnumShellItems</b> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumShellItems</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumShellItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumShellItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumshellitems-clone">Clone</a>
</td>
<td align="left" width="63%">
Gets a copy of the current enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumshellitems-next">Next</a>
</td>
<td align="left" width="63%">
Gets an array of one or more <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interfaces from the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumshellitems-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the internal count of retrieved <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interfaces in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumshellitems-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a given number of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> interfaces in the enumeration. Used when retrieving interfaces.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>