---
UID: NN:shobjidl_core.ICategorizer
title: ICategorizer (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that are used to obtain information about item identifier lists.
old-location: shell\ICategorizer.htm
tech.root: shell
ms.assetid: 59c80328-0f82-4289-b55d-045f0cd3dc81
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICategorizer, ICategorizer interface [Windows Shell], ICategorizer interface [Windows Shell],described, inet_ICategorizer, shell.ICategorizer, shobjidl_core/ICategorizer
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/ICategorizer"
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
 - ICategorizer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICategorizer interface


## -description


Exposes methods that are used to obtain information about item identifier lists.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICategorizer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICategorizer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICategorizer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategorizer-comparecategory">CompareCategory</a>
</td>
<td align="left" width="63%">
Determines the relative order of two items in their item identifier lists, and hence in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategorizer-getcategory">GetCategory</a>
</td>
<td align="left" width="63%">
Gets a list of categories associated with a list of identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategorizer-getcategoryinfo">GetCategoryInfo</a>
</td>
<td align="left" width="63%">
Gets information about a category, such as the default display and the text to display in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategorizer-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Gets the name of a categorizer, such as <i>Group By Device Type</i>, that can be displayed in the UI.

</td>
</tr>
</table> 

