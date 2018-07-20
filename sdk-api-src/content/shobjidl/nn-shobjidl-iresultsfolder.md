---
UID: NN:shobjidl.IResultsFolder
title: IResultsFolder
author: windows-sdk-content
description: Exposes methods that hold items from a data object.
old-location: shell\IResultsFolder.htm
old-project: shell
ms.assetid: db44052b-bd26-412f-9f2a-66a0c53b65ac
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IResultsFolder, IResultsFolder interface [Windows Shell], IResultsFolder interface [Windows Shell],described, _shell_IResultsFolder, shell.IResultsFolder, shobjidl/IResultsFolder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IResultsFolder
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IResultsFolder interface


## -description


Exposes methods that hold items from a data object.

An <b>IResultsFolder</b> is a folder that can hold items from all over the namespace and represent them to the user in a single folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultsFolder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IResultsFolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IResultsFolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0514fe4d-87d3-4665-a35b-9f9788fc169d">AddIDList</a>
</td>
<td align="left" width="63%">
Inserts a PIDL into a results folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/005f7125-8dc2-4d9c-a860-1bb56b4d0b63">AddItem</a>
</td>
<td align="left" width="63%">
Adds an item to a results folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2aac1b5a-298a-4682-9874-7cf114ce1f63">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all items from a results folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/188d4f7f-954c-4bba-ad4e-164085e0cc5a">RemoveIDList</a>
</td>
<td align="left" width="63%">
Removes a PIDL from a results folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17be32ed-50d7-4c16-9a06-97c4a0f8dc8d">RemoveItem</a>
</td>
<td align="left" width="63%">
Removes an item from a results folder.

</td>
</tr>
</table> 

