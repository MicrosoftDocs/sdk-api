---
UID: NN:shlobj_core.IShellIconOverlayManager
title: IShellIconOverlayManager (shlobj_core.h)
description: IShellIconOverlayManager may be altered or unavailable.
helpviewer_keywords: ["IShellIconOverlayManager","IShellIconOverlayManager interface [Windows Shell]","IShellIconOverlayManager interface [Windows Shell]","described","_win32_IShellIconOverlayManager","shell.IShellIconOverlayManager","shlobj_core/IShellIconOverlayManager"]
old-location: shell\IShellIconOverlayManager.htm
tech.root: shell
ms.assetid: 769c3b0b-ece4-4406-a76c-cabc37901351
ms.date: 12/05/2018
ms.keywords: IShellIconOverlayManager, IShellIconOverlayManager interface [Windows Shell], IShellIconOverlayManager interface [Windows Shell],described, _win32_IShellIconOverlayManager, shell.IShellIconOverlayManager, shlobj_core/IShellIconOverlayManager
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IShellIconOverlayManager
 - shlobj_core/IShellIconOverlayManager
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
 - IShellIconOverlayManager
---

# IShellIconOverlayManager interface


## -description

<p class="CCE_Message">[<b>IShellIconOverlayManager</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes methods that retrieve the icon overlay information, including the overlay index and the image index for an IShellFolder object. This interface iterates through all the icon overlay IDs and keeps the information in an array.

## -inheritance

The <b>IShellIconOverlayManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellIconOverlayManager</b> also has these types of members:

## -remarks

Icon overlays are small images placed at the lower-left corner of the icon that represents a Shell object in Windows Explorer or on the desktop. They are used to add some extra information to the object's normal icon. A commonly used icon overlay is the small arrow that indicates that a file or folder is actually a link. For more information, see <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay">IShellIconOverlay</a>.

This interface must be implemented by all icon overlay handlers.

This interface is not typically called by applications.
