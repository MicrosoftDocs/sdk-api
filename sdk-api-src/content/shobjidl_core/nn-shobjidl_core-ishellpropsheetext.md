---
UID: NN:shobjidl_core.IShellPropSheetExt
title: IShellPropSheetExt (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that allow a property sheet handler to add or replace pages in the property sheet displayed for a file object.
old-location: shell\IShellPropSheetExt.htm
tech.root: shell
ms.assetid: 1671ad3e-c131-4de0-a213-b22c9966bae2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellPropSheetExt, IShellPropSheetExt interface [Windows Shell], IShellPropSheetExt interface [Windows Shell],described, _win32_IShellPropSheetExt, _win32_ishellpropsheetext_cpp, shell.IShellPropSheetExt, shobjidl_core/IShellPropSheetExt
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IShellPropSheetExt"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellPropSheetExt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellPropSheetExt interface


## -description


Exposes methods that allow a property sheet handler to add or replace pages in the property sheet displayed for a file object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellPropSheetExt</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellPropSheetExt</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages">AddPages</a>
</td>
<td align="left" width="63%">
Adds one or more pages to a property sheet that the Shell displays for a file object. The Shell calls this method for each property sheet handler registered to the file type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage">ReplacePage</a>
</td>
<td align="left" width="63%">
Replaces a page in a property sheet for a Control Panel object.

</td>
</tr>
</table> 

