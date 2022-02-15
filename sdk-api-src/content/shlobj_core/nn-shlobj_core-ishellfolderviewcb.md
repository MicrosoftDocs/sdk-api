---
UID: NN:shlobj_core.IShellFolderViewCB
title: IShellFolderViewCB (shlobj_core.h)
description: Exposes a method that allows communication between Windows Explorer and a folder view implemented using the system folder view object (the IShellView object returned through SHCreateShellFolderView) so that the folder view can be notified of events and modify its view accordingly.
helpviewer_keywords: ["IShellFolderViewCB","IShellFolderViewCB interface [Windows Shell]","IShellFolderViewCB interface [Windows Shell]","described","_win32_IShellFolderViewCB","shell.IShellFolderViewCB","shlobj_core/IShellFolderViewCB"]
old-location: shell\IShellFolderViewCB.htm
tech.root: shell
ms.assetid: 0cd2bce8-d77a-4140-869b-707aaa279796
ms.date: 12/05/2018
ms.keywords: IShellFolderViewCB, IShellFolderViewCB interface [Windows Shell], IShellFolderViewCB interface [Windows Shell],described, _win32_IShellFolderViewCB, shell.IShellFolderViewCB, shlobj_core/IShellFolderViewCB
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolderViewCB
 - shlobj_core/IShellFolderViewCB
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
 - IShellFolderViewCB
---

# IShellFolderViewCB interface


## -description

Exposes a method that allows communication between Windows Explorer and a folder view implemented using the system folder view object (the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> object returned through <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a>) so that the folder view can be notified of events and modify its view accordingly.

## -inheritance

The <b>IShellFolderViewCB</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellFolderViewCB</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-lpfnviewcallback">LPFNVIEWCALLBACK</a>
