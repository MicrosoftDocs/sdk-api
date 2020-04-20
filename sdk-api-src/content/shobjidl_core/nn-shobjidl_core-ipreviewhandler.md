---
UID: NN:shobjidl_core.IPreviewHandler
title: IPreviewHandler (shobjidl_core.h)
description: Exposes methods for the display of rich previews.helpviewer_keywords: ["IPreviewHandler","IPreviewHandler interface [Windows Shell]","IPreviewHandler interface [Windows Shell]","described","_shell_IPreviewHandler","shell.IPreviewHandler","shobjidl_core/IPreviewHandler"]
old-location: shell\IPreviewHandler.htm
tech.root: shell
ms.assetid: a4e6507c-10b1-4c21-9359-92ba635a2a2c
ms.date: 12/05/2018
ms.keywords: IPreviewHandler, IPreviewHandler interface [Windows Shell], IPreviewHandler interface [Windows Shell],described, _shell_IPreviewHandler, shell.IPreviewHandler, shobjidl_core/IPreviewHandler
f1_keywords:
- shobjidl_core/IPreviewHandler
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IPreviewHandler
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
ms.custom: 19H1
---

# IPreviewHandler interface


## -description


Exposes methods for the display of rich previews.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPreviewHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPreviewHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPreviewHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview">DoPreview</a>
</td>
<td align="left" width="63%">
Directs the preview handler to load data from the source specified in an earlier Initialize method call, and to begin rendering to the previewer window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-queryfocus">QueryFocus</a>
</td>
<td align="left" width="63%">
Directs the preview handler to return the <b>HWND</b> from calling the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getfocus">GetFocus Function</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setfocus">SetFocus</a>
</td>
<td align="left" width="63%">
Directs the preview handler to set focus to itself.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect">SetRect</a>
</td>
<td align="left" width="63%">
Directs the preview handler to change the area within the parent hwnd that it draws into.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow">SetWindow</a>
</td>
<td align="left" width="63%">
Sets the parent window of the previewer window, as well as the area within the parent to be used for the previewer window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-translateaccelerator">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Directs the preview handler to handle a keystroke passed up from the message pump of the process in which the preview handler is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload">Unload</a>
</td>
<td align="left" width="63%">
Directs the preview handler to cease rendering a preview and to release all resources that have been allocated based on the item passed in during the initialization.

</td>
</tr>
</table> 


## -remarks



Preview handlers can be built in managed code. Typically, all preview handlers are hosted together in a surrogate process called prevhost.exe. There is one instance of this process for preview handlers running at normal integrity level, and another instance for preview handlers running at low integrity level. If you want to implement your handler in managed code, your handler should not run inside either of these shared processes. Instead, arrange for your handler to get a new instance of prevhost.exe by creating a new AppID entry in the registry (specifying prevhost.exe as the DllSurrogate value) and then setting that as the AppID value in the registry value for your handler's class ID. This will ensure that a unique prevhost.exe instance is created for your handler, instead of the common instances used by the other handlers.
            



