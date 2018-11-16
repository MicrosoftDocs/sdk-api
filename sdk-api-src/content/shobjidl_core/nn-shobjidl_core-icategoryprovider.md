---
UID: NN:shobjidl_core.ICategoryProvider
title: ICategoryProvider
author: windows-sdk-content
description: Exposes a list of categorizers registered on an IShellFolder.
old-location: shell\ICategoryProvider.htm
tech.root: shell
ms.assetid: bab74832-6f24-4f3a-b8cb-68506f293b3c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICategoryProvider, ICategoryProvider interface [Windows Shell], ICategoryProvider interface [Windows Shell],described, inet_ICategoryProvider, shell.ICategoryProvider, shobjidl_core/ICategoryProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICategoryProvider interface


## -description


Exposes a list of categorizers registered on an <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICategoryProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICategoryProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e0b10007-7b25-4ddf-8cb9-76d85f8fb4df">CanCategorizeOnSCID</a>
</td>
<td align="left" width="63%">
Determines whether a column can be used as a category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3703c061-4d21-4c36-900a-9ccacf4d482a">CreateCategory</a>
</td>
<td align="left" width="63%">
Creates a category object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5008ce75-7a90-4f30-84e0-13d00cc1e58e">EnumCategories</a>
</td>
<td align="left" width="63%">
Gets the enumerator for the list of GUIDs that represent categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52b4fac7-14bd-4d58-a00d-f102e013df16">GetCategoryForSCID</a>
</td>
<td align="left" width="63%">
Gets a GUID that represents the categorizer to use for the specified Shell column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3730394a-8720-46cc-a9da-cd5cf0df7eeb">GetCategoryName</a>
</td>
<td align="left" width="63%">
Gets the name of the specified category.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5a5d04c-b666-4063-bf0b-02564aa967ab">GetDefaultCategory</a>
</td>
<td align="left" width="63%">
Enables the folder to override the default grouping.

</td>
</tr>
</table> 

