---
UID: NN:shobjidl_core.IShellItemResources
title: IShellItemResources (shobjidl_core.h)
description: Exposes methods to manipulate and query Shell item resources.
helpviewer_keywords: ["IShellItemResources","IShellItemResources interface [Windows Shell]","IShellItemResources interface [Windows Shell]","described","_shell_IShellItemResources","shell.IShellItemResources","shobjidl_core/IShellItemResources"]
old-location: shell\IShellItemResources.htm
tech.root: shell
ms.assetid: 4ca4a01e-e3c2-46aa-a700-b4b2a1e0112e
ms.date: 12/05/2018
ms.keywords: IShellItemResources, IShellItemResources interface [Windows Shell], IShellItemResources interface [Windows Shell],described, _shell_IShellItemResources, shell.IShellItemResources, shobjidl_core/IShellItemResources
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
 - IShellItemResources
 - shobjidl_core/IShellItemResources
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
 - IShellItemResources
---

# IShellItemResources interface


## -description

Exposes methods to manipulate and query Shell item resources.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellItemResources</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellItemResources</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellItemResources</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemresources-createresource">CreateResource</a>
</td>
<td align="left" width="63%">
Creates a specified resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemresources-enumresources">EnumResources</a>
</td>
<td align="left" width="63%">
Gets a resource enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemresources-getattributes">GetAttributes</a>
</td>
<td align="left" width="63%">
Gets resource attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemresources-getresourcedescription">GetResourceDescription</a>
</td>
<td align="left" width="63%">
Gets a resource description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemresources-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Gets the source size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemresources-gettimes">GetTimes</a>
</td>
<td align="left" width="63%">
Gets file times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemresources-markfordelete">MarkForDelete</a>
</td>
<td align="left" width="63%">
Marks for delete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemresources-openresource">OpenResource</a>
</td>
<td align="left" width="63%">
Opens a specified resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemresources-settimes">SetTimes</a>
</td>
<td align="left" width="63%">
Sets file times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemresources-supportsresource">SupportsResource</a>
</td>
<td align="left" width="63%">
Retrieves whether an item supports a specified resource.

</td>
</tr>
</table>

