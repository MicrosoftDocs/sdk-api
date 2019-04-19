---
UID: NF:shobjidl_core.ITaskbarList2.MarkFullscreenWindow
title: ITaskbarList2::MarkFullscreenWindow (shobjidl_core.h)
author: windows-sdk-content
description: Marks a window as full-screen.
old-location: shell\ITaskbarList2_MarkFullscreenWindow.htm
tech.root: shell
ms.assetid: 17b4a9ff-f5a2-4178-971b-f80d65d72fb5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITaskbarList2 interface [Windows Shell],MarkFullscreenWindow method, ITaskbarList2.MarkFullscreenWindow, ITaskbarList2::MarkFullscreenWindow, MarkFullscreenWindow, MarkFullscreenWindow method [Windows Shell], MarkFullscreenWindow method [Windows Shell],ITaskbarList2 interface, shell.ITaskbarList2_MarkFullscreenWindow, shell_ITaskbarList2_MarkFullscreenWindow, shobjidl_core/ITaskbarList2::MarkFullscreenWindow
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ITaskbarList2.MarkFullscreenWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskbarList2::MarkFullscreenWindow


## -description


Marks a window as full-screen.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window to be marked.


### -param fFullscreen [in]

Type: <b>BOOL</b>

A Boolean value marking the desired full-screen status of the window.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Setting the value of <i>fFullscreen</i> to <b>TRUE</b>, the Shell treats this window as a full-screen window, and the taskbar is moved to the bottom of the z-order when this window is active. Setting the value of <i>fFullscreen</i> to <b>FALSE</b> removes the full-screen marking, but <i>does not</i> cause the Shell to treat the window as though it were definitely not full-screen. With a <b>FALSE</b> <i>fFullscreen</i> value, the Shell depends on its automatic detection facility to specify how the window should be treated, possibly still flagging the window as full-screen.




## -see-also




<a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>



<a href="https://msdn.microsoft.com/8af23586-349f-4d21-98cb-0aaa27a586ff">ITaskbarList2</a>
 

 

