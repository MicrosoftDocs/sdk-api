---
UID: NN:shobjidl_core.ICategorizer
title: ICategorizer
author: windows-sdk-content
description: Exposes methods that are used to obtain information about item identifier lists.
old-location: shell\ICategorizer.htm
old-project: shell
ms.assetid: 59c80328-0f82-4289-b55d-045f0cd3dc81
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ICategorizer, ICategorizer interface [Windows Shell], ICategorizer interface [Windows Shell],described, inet_ICategorizer, shell.ICategorizer, shobjidl_core/ICategorizer
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	ICategorizer
product: Windows
targetos: Windows
req.lib: Twinapi.lib
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# ICategorizer interface


## -description


Exposes methods that are used to obtain information about item identifier lists.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICategorizer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICategorizer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/25775fa5-595d-4911-9cd4-47fde429b923">CompareCategory</a>
</td>
<td align="left" width="63%">
Determines the relative order of two items in their item identifier lists, and hence in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3756e9e-7d68-4e30-92d4-1fddccf66ba5">GetCategory</a>
</td>
<td align="left" width="63%">
Gets a list of categories associated with a list of identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b789033-ce42-4fb5-8a3d-b05243b62d4e">GetCategoryInfo</a>
</td>
<td align="left" width="63%">
Gets information about a category, such as the default display and the text to display in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Gets the name of a categorizer, such as <i>Group By Device Type</i>, that can be displayed in the UI.

</td>
</tr>
</table> 

