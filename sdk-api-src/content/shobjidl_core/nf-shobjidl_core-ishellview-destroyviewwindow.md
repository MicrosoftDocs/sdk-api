---
UID: NF:shobjidl_core.IShellView.DestroyViewWindow
title: IShellView::DestroyViewWindow
author: windows-sdk-content
description: Destroys the view window.
old-location: shell\IShellView_DestroyViewWindow.htm
old-project: shell
ms.assetid: b0dfc200-4438-4f11-a426-c82eeb9cc745
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DestroyViewWindow, DestroyViewWindow method [Windows Shell], DestroyViewWindow method [Windows Shell],IShellView interface, IShellView interface [Windows Shell],DestroyViewWindow method, IShellView.DestroyViewWindow, IShellView::DestroyViewWindow, _win32_IShellView_DestroyViewWindow, shell.IShellView_DestroyViewWindow, shobjidl_core/IShellView::DestroyViewWindow
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellView.DestroyViewWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellView::DestroyViewWindow


## -description


Destroys the view window.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.




## -remarks



Windows Explorer calls this method when a folder window or Windows Explorer is being closed.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Clean up all states that represent the view, including the window and any other associated resources.




## -see-also




<a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>
 

 

