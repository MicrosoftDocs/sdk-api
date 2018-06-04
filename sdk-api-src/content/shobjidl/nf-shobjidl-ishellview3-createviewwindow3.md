---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IShellView3::CreateViewWindow3


## -description


Requests the creation of a new Shell view window. The view can be either the right pane of Windows Explorer or the client window of a folder window. This method replaces <a href="https://msdn.microsoft.com/3b829f5f-26ea-4987-be05-6725eeff5fed">CreateViewWindow2</a>.


## -parameters




### -param psbOwner [in]

Type: <b><a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a> interface to provide namespace extension services.


### -param psvPrev [in]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface that represents the previous view in the Windows Explorer or folder window.


### -param dwViewFlags [in]

Type: <b>SV3CVW3_FLAGS</b>

Flags that specify details of the view being created.



#### SV3CVW3_DEFAULT

The default view.



#### SV3CVW3_NONINTERACTIVE

In the case of an error, the view should fail silently rather than displaying a UI.



#### SV3CVW3_FORCEVIEWMODE

The view mode set by <b>IShellView3::CreateViewWindow3</b> overrides the saved view state.



#### SV3CVW3_FORCEFOLDERFLAGS

Folder flags set by <b>IShellView3::CreateViewWindow3</b> override the saved view state.


### -param dwMask [in]

Type: <b><a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a></b>

A bitwise mask that specifies which folder options specified in <i>dwFlags</i> are to be used.


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a></b>

A bitwise value that contains the folder options, as <a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a>, to use in the new view.


### -param fvMode [in]

Type: <b><a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a></b>

A bitwise value that contains the folder view mode options, as <a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a>, to use in the new view.


### -param pvid [in]

Type: <b>const SHELLVIEWID*</b>

A pointer to Shell view ID as a <b>GUID</b>.


### -param prcView [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <b>RECT</b> structure that provides the dimensions of the view window.


### -param phwndView [out]

Type: <b>HWND*</b>

A value that receives a pointer to the handle of the new Shell view window.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



