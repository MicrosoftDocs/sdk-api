---
UID: NN:shobjidl_core.IShellPropSheetExt
title: IShellPropSheetExt
author: windows-sdk-content
description: Exposes methods that allow a property sheet handler to add or replace pages in the property sheet displayed for a file object.
old-location: shell\IShellPropSheetExt.htm
old-project: shell
ms.assetid: 1671ad3e-c131-4de0-a213-b22c9966bae2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellPropSheetExt, IShellPropSheetExt interface [Windows Shell], IShellPropSheetExt interface [Windows Shell],described, _win32_IShellPropSheetExt, _win32_ishellpropsheetext_cpp, shell.IShellPropSheetExt, shobjidl_core/IShellPropSheetExt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellPropSheetExt
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellPropSheetExt interface


## -description


Exposes methods that allow a property sheet handler to add or replace pages in the property sheet displayed for a file object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellPropSheetExt</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellPropSheetExt</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellPropSheetExt</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76a2a94b-b79f-41d1-9e42-fbfda545d12f">AddPages</a>
</td>
<td align="left" width="63%">
Adds one or more pages to a property sheet that the Shell displays for a file object. The Shell calls this method for each property sheet handler registered to the file type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0addd55c-756e-41f6-998e-0f464b609aac">ReplacePage</a>
</td>
<td align="left" width="63%">
Replaces a page in a property sheet for a Control Panel object.

</td>
</tr>
</table> 

