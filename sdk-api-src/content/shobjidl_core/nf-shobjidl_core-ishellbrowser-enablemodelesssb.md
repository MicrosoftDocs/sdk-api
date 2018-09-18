---
UID: NF:shobjidl_core.IShellBrowser.EnableModelessSB
title: IShellBrowser::EnableModelessSB
author: windows-sdk-content
description: Tells Windows Explorer to enable or disable its modeless dialog boxes.
old-location: shell\IShellBrowser_EnableModelessSB.htm
tech.root: shell
ms.assetid: 6bf39e3f-8b17-4307-ba57-7363c006c34b
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: EnableModelessSB, EnableModelessSB method [Windows Shell], EnableModelessSB method [Windows Shell],IShellBrowser interface, IShellBrowser interface [Windows Shell],EnableModelessSB method, IShellBrowser.EnableModelessSB, IShellBrowser::EnableModelessSB, _win32_IShellBrowser_EnableModelessSB, shell.IShellBrowser_EnableModelessSB, shobjidl_core/IShellBrowser::EnableModelessSB
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IShellBrowser.EnableModelessSB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellBrowser::EnableModelessSB


## -description


Tells Windows Explorer to enable or disable its modeless dialog boxes.


## -parameters




### -param fEnable

Type: <b>BOOL</b>

Specifies whether the modeless dialog boxes are to be enabled or disabled. If this parameter is nonzero, modeless dialog boxes are enabled. If this parameter is zero, modeless dialog boxes are disabled.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or a COM-defined error value otherwise.




## -remarks



This method is similar to the <a href="https://msdn.microsoft.com/4c6ea1ee-861d-45ff-a9d2-d3b241f00c9f">IOleInPlaceFrame::EnableModeless</a> method. Although the current version of Windows Explorer does not have any modeless dialog boxes, the view should call this method when it wants to disable or enable modeless dialog boxes associated with the Windows Explorer window.




## -see-also




<a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>
 

 

