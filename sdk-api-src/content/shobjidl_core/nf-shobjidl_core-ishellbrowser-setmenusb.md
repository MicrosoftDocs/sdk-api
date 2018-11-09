---
UID: NF:shobjidl_core.IShellBrowser.SetMenuSB
title: IShellBrowser::SetMenuSB
author: windows-sdk-content
description: Installs the composite menu in the view window.
old-location: shell\IShellBrowser_SetMenuSB.htm
tech.root: shell
ms.assetid: ae6fe864-7fa1-4c74-a27f-d428bdeccc3d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IShellBrowser interface [Windows Shell],SetMenuSB method, IShellBrowser.SetMenuSB, IShellBrowser::SetMenuSB, SetMenuSB, SetMenuSB method [Windows Shell], SetMenuSB method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_SetMenuSB, shell.IShellBrowser_SetMenuSB, shobjidl_core/IShellBrowser::SetMenuSB
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
 - IShellBrowser.SetMenuSB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellBrowser::SetMenuSB


## -description


Installs the composite menu in the view window.


## -parameters




### -param hmenuShared

Type: <b>HMENU</b>

A handle to the composite menu constructed by calls to <a href="https://msdn.microsoft.com/62cbb593-7459-4a4f-96a2-3ec2287e6a26">IShellBrowser::InsertMenusSB</a> and the <a href="https://msdn.microsoft.com/8ca7510a-e035-4ba2-98dd-57d777cae814">InsertMenu</a> function.


### -param holemenuRes

Type: <b>HOLEMENU</b>


### -param hwndActiveObject

Type: <b>HWND</b>

The view's window handle.


## -returns



Type: <b>RESULT</b>

Returns <b>S_OK</b> if successful, or a COM-defined error value otherwise.




## -remarks



This method is similar to the <a href="https://msdn.microsoft.com/dc26a399-846d-4d15-b406-752350e528c2">IOleInPlaceFrame::SetMenu</a> method. However, Windows Explorer performs menu dispatch based on the menu item identifier.

The availability of specific menu items depends on whether the view has the focus. Accordingly, it is necessary to call the <a href="https://msdn.microsoft.com/bd320262-f383-453b-9028-4e93f0b3761a">IShellBrowser::OnViewWindowActive</a> method whenever the view window (or one of its child windows) has the focus.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
The object calls <b>IShellBrowser_SetMenuSB</b> to ask the container to install the composite menu structure set up by calls to <a href="https://msdn.microsoft.com/62cbb593-7459-4a4f-96a2-3ec2287e6a26">IShellBrowser::InsertMenusSB</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
A container's implementation of this method should call the <b>SetMenu</b> function.




## -see-also




<a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>
 

 

