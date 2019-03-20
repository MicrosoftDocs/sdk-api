---
UID: NN:shlobj.INewShortcutHookW
title: INewShortcutHookW (shlobj.h)
author: windows-sdk-content
description: Exposes methods to create a new Internet shortcut.
old-location: shell\INewShortcutHook.htm
tech.root: shell
ms.assetid: 5a097e96-178a-44bd-9d3d-ed53338b97d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INewShortcutHook, INewShortcutHook interface [Windows Shell], INewShortcutHook interface [Windows Shell],described, INewShortcutHookA, INewShortcutHookW, _win32_INewShortcutHook, shell.INewShortcutHook, shlobj/INewShortcutHook
ms.topic: interface
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - INewShortcutHook
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INewShortcutHookW interface


## -description


Exposes methods to create a new Internet shortcut.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INewShortcutHook</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INewShortcutHook</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INewShortcutHook</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccb54291-7c87-4783-af25-549704371878">GetExtension</a>
</td>
<td align="left" width="63%">
Gets the file name extension for the shortcut object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b743242-3ebe-46cb-a084-575228cb314b">GetFolder</a>
</td>
<td align="left" width="63%">
Gets the folder name for the shortcut object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5eb4a3ce-74ce-4b97-bb5e-67cab82401ec">GetName</a>
</td>
<td align="left" width="63%">
Gets the file name of the shortcut object, without the extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/856f15bb-f9a8-4114-9a18-5abc21bef534">GetReferent</a>
</td>
<td align="left" width="63%">
Gets the referent of the shortcut object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f402d36-58cf-4912-af21-f8271eee98e4">SetFolder</a>
</td>
<td align="left" width="63%">
Sets the folder name for the shortcut object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/402d305e-1657-45c2-9f0d-04703c8d6e5c">SetReferent</a>
</td>
<td align="left" width="63%">
Sets the referent of the shortcut object.

</td>
</tr>
</table> 


## -remarks



You do not typically implement <b>INewShortcutHook</b>. It is implemented by the Shell for Internet shortcuts.

You use <b>INewShortcutHook</b> when creating a new Internet shortcut. The methods provided by this interface are supplied as a convenience.

<b>INewShortcutHook</b> is derived from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. The listed methods are specific to <b>INewShortcutHook</b>.



