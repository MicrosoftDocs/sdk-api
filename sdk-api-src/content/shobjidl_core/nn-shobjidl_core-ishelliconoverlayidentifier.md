---
UID: NN:shobjidl_core.IShellIconOverlayIdentifier
title: IShellIconOverlayIdentifier (shobjidl_core.h)
description: Exposes methods that handle all communication between icon overlay handlers and the Shell.
helpviewer_keywords: ["IShellIconOverlayIdentifier","IShellIconOverlayIdentifier interface [Windows Shell]","IShellIconOverlayIdentifier interface [Windows Shell]","described","_win32_IShellIconOverlayIdentifier","shell.IShellIconOverlayIdentifier","shobjidl_core/IShellIconOverlayIdentifier"]
old-location: shell\IShellIconOverlayIdentifier.htm
tech.root: shell
ms.assetid: c093bc13-def7-411d-b741-50996ffad84b
ms.date: 12/05/2018
ms.keywords: IShellIconOverlayIdentifier, IShellIconOverlayIdentifier interface [Windows Shell], IShellIconOverlayIdentifier interface [Windows Shell],described, _win32_IShellIconOverlayIdentifier, shell.IShellIconOverlayIdentifier, shobjidl_core/IShellIconOverlayIdentifier
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellIconOverlayIdentifier
 - shobjidl_core/IShellIconOverlayIdentifier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellIconOverlayIdentifier
---

# IShellIconOverlayIdentifier interface


## -description

Exposes methods that handle all communication between icon overlay handlers and the Shell.

## -inheritance

The <b>IShellIconOverlayIdentifier</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellIconOverlayIdentifier</b> also has these types of members:

## -remarks

Icon overlays are small images placed at the lower-left corner of the icon that represents a Shell object in Windows Explorer or on the desktop. They are used to add some extra information to the object's normal icon. A commonly used icon overlay is the small arrow that indicates that a file or folder is actually a link. You can specify custom icon overlays for Shell objects by implementing and registering an icon overlay handler.

Icon overlay handlers are Component Object Model (COM) objects that are associated with a particular icon overlay. For a general discussion of icon overlay handlers, see <a href="/windows/desktop/shell/how-to-implement-icon-overlay-handlers">How to Implement Icon Overlay Handlers</a>.

This interface must be implemented by all icon overlay handlers.

This interface is not typically called by applications.
