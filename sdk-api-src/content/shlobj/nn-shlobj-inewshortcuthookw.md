---
UID: NN:shlobj.INewShortcutHookW
title: INewShortcutHookW (shlobj.h)
author: windows-sdk-content
description: Exposes methods to create a new Internet shortcut.
old-location: shell\INewShortcutHook.htm
tech.root: shell
ms.assetid: 5a097e96-178a-44bd-9d3d-ed53338b97d5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INewShortcutHook, INewShortcutHook interface [Windows Shell], INewShortcutHook interface [Windows Shell],described, INewShortcutHookA, INewShortcutHookW, _win32_INewShortcutHook, shell.INewShortcutHook, shlobj/INewShortcutHook
ms.topic: interface
f1_keywords: 
 - "shlobj/INewShortcutHook"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INewShortcutHookW interface


## -description


Exposes methods to create a new Internet shortcut.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INewShortcutHook</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INewShortcutHook</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-inewshortcuthooka-getextension">GetExtension</a>
</td>
<td align="left" width="63%">
Gets the file name extension for the shortcut object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-inewshortcuthooka-getfolder">GetFolder</a>
</td>
<td align="left" width="63%">
Gets the folder name for the shortcut object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-inewshortcuthooka-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the file name of the shortcut object, without the extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-inewshortcuthooka-getreferent">GetReferent</a>
</td>
<td align="left" width="63%">
Gets the referent of the shortcut object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-inewshortcuthooka-setfolder">SetFolder</a>
</td>
<td align="left" width="63%">
Sets the folder name for the shortcut object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-inewshortcuthooka-setreferent">SetReferent</a>
</td>
<td align="left" width="63%">
Sets the referent of the shortcut object.

</td>
</tr>
</table> 


## -remarks



You do not typically implement <b>INewShortcutHook</b>. It is implemented by the Shell for Internet shortcuts.

You use <b>INewShortcutHook</b> when creating a new Internet shortcut. The methods provided by this interface are supplied as a convenience.

<b>INewShortcutHook</b> is derived from <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>. The listed methods are specific to <b>INewShortcutHook</b>.



