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

# IShellBrowser::GetControlWindow


## -description


Gets the window handle to a browser control.


## -parameters




### -param id

Type: <b>UINT</b>

The control handle that is being requested. This parameter can be one of the following values: 



#### FCW_TOOLBAR

Retrieves the window handle to the browser's toolbar.



#### FCW_STATUS

Retrieves the window handle to the browser's status bar.



#### FCW_TREE

Retrieves the window handle to the browser's tree view.



#### FCW_PROGRESS

Retrieves the window handle to the browser's progress bar.


### -param phwnd






#### - lphwnd

Type: <b>HWND*</b>

The address of the window handle to the Windows Explorer control.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.




## -remarks



<b>GetControlWindow</b> is used so views can directly manipulate the browser's controls. <b>FCW_TREE</b> should be used only to determine if the tree is present.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
<b>GetControlWindow</b> is used to manipulate and test the state of the control windows. Do not send messages directly to these controls; instead, use <a href="https://msdn.microsoft.com/4494870b-45a8-478a-807a-7ed3674f69f3">IShellBrowser::SendControlMsg</a>. Be prepared for this method to return <b>NULL</b>. Later versions of Windows Explorer may not include a toolbar, status bar, or tree window.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
<b>GetControlWindow</b> returns the window handle to these controls if they exist in your implementation.

See also <a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>




