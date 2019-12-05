---
UID: NN:shobjidl_core.ICategoryProvider
title: ICategoryProvider (shobjidl_core.h)
description: Exposes a list of categorizers registered on an IShellFolder.
old-location: shell\ICategoryProvider.htm
tech.root: shell
ms.assetid: bab74832-6f24-4f3a-b8cb-68506f293b3c
ms.date: 12/05/2018
ms.keywords: ICategoryProvider, ICategoryProvider interface [Windows Shell], ICategoryProvider interface [Windows Shell],described, inet_ICategoryProvider, shell.ICategoryProvider, shobjidl_core/ICategoryProvider
ms.topic: interface
f1_keywords:
- shobjidl_core/ICategoryProvider
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- ICategoryProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICategoryProvider interface


## -description


Exposes a list of categorizers registered on an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICategoryProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICategoryProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICategoryProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategoryprovider-cancategorizeonscid">CanCategorizeOnSCID</a>
</td>
<td align="left" width="63%">
Determines whether a column can be used as a category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategoryprovider-createcategory">CreateCategory</a>
</td>
<td align="left" width="63%">
Creates a category object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategoryprovider-enumcategories">EnumCategories</a>
</td>
<td align="left" width="63%">
Gets the enumerator for the list of GUIDs that represent categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategoryprovider-getcategoryforscid">GetCategoryForSCID</a>
</td>
<td align="left" width="63%">
Gets a GUID that represents the categorizer to use for the specified Shell column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategoryprovider-getcategoryname">GetCategoryName</a>
</td>
<td align="left" width="63%">
Gets the name of the specified category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategoryprovider-getdefaultcategory">GetDefaultCategory</a>
</td>
<td align="left" width="63%">
Enables the folder to override the default grouping.

</td>
</tr>
</table> 

