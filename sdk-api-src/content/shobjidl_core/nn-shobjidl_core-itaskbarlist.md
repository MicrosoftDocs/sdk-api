---
UID: NN:shobjidl_core.ITaskbarList
title: ITaskbarList (shobjidl_core.h)
description: Exposes methods that control the taskbar. It allows you to dynamically add, remove, and activate items on the taskbar.
helpviewer_keywords: ["ITaskbarList","ITaskbarList interface [Windows Shell]","ITaskbarList interface [Windows Shell]","described","_win32_ITaskbarList","shell.ITaskbarList","shobjidl_core/ITaskbarList"]
old-location: shell\ITaskbarList.htm
tech.root: shell
ms.assetid: c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38
ms.date: 12/05/2018
ms.keywords: ITaskbarList, ITaskbarList interface [Windows Shell], ITaskbarList interface [Windows Shell],described, _win32_ITaskbarList, shell.ITaskbarList, shobjidl_core/ITaskbarList
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskbarList
 - shobjidl_core/ITaskbarList
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
 - ITaskbarList
---

# ITaskbarList interface


## -description

Exposes methods that control the taskbar. It allows you to dynamically add, remove, and activate items on the taskbar.

## -inheritance

The <b>ITaskbarList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskbarList</b> also has these types of members:

## -remarks

You do not implement <b>ITaskbarList</b>; it is implemented by the Shell.

Use <b>ITaskbarList</b> to add items to the taskbar, remove items from the taskbar, and activate items on the taskbar.

See <a href="/windows/desktop/shell/taskbar">Modifying Contents of the Taskbar</a> for more information about using this interface.
