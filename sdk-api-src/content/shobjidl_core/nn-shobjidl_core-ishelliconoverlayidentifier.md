---
UID: NN:shobjidl_core.IShellIconOverlayIdentifier
title: IShellIconOverlayIdentifier (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that handle all communication between icon overlay handlers and the Shell.
old-location: shell\IShellIconOverlayIdentifier.htm
tech.root: shell
ms.assetid: c093bc13-def7-411d-b741-50996ffad84b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellIconOverlayIdentifier, IShellIconOverlayIdentifier interface [Windows Shell], IShellIconOverlayIdentifier interface [Windows Shell],described, _win32_IShellIconOverlayIdentifier, shell.IShellIconOverlayIdentifier, shobjidl_core/IShellIconOverlayIdentifier
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IShellIconOverlayIdentifier"
req.header: shobjidl_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellIconOverlayIdentifier
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellIconOverlayIdentifier interface


## -description


Exposes methods that handle all communication between icon overlay handlers and the Shell.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellIconOverlayIdentifier</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellIconOverlayIdentifier</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellIconOverlayIdentifier</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo">GetOverlayInfo</a>
</td>
<td align="left" width="63%">
Provides the location of the icon overlay's bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority">GetPriority</a>
</td>
<td align="left" width="63%">
Specifies the priority of an icon overlay.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof">IsMemberOf</a>
</td>
<td align="left" width="63%">
Specifies whether an icon overlay should be added to a Shell object's icon.

</td>
</tr>
</table> 


## -remarks



Icon overlays are small images placed at the lower-left corner of the icon that represents a Shell object in Windows Explorer or on the desktop. They are used to add some extra information to the object's normal icon. A commonly used icon overlay is the small arrow that indicates that a file or folder is actually a link. You can specify custom icon overlays for Shell objects by implementing and registering an icon overlay handler.

Icon overlay handlers are Component Object Model (COM) objects that are associated with a particular icon overlay. For a general discussion of icon overlay handlers, see <a href="https://docs.microsoft.com/windows/desktop/shell/how-to-implement-icon-overlay-handlers">How to Implement Icon Overlay Handlers</a>.

This interface must be implemented by all icon overlay handlers.

This interface is not typically called by applications.



