---
UID: NF:shobjidl_core.IShellBrowser.RemoveMenusSB
title: IShellBrowser::RemoveMenusSB
author: windows-driver-content
description: Permits the container to remove any of its menu elements from the in-place composite menu and to free all associated resources.
old-location: shell\IShellBrowser_RemoveMenusSB.htm
old-project: shell
ms.assetid: aa96ac59-62cd-4010-8a0f-b743527f61da
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IShellBrowser interface [Windows Shell],RemoveMenusSB method, IShellBrowser.RemoveMenusSB, IShellBrowser::RemoveMenusSB, RemoveMenusSB, RemoveMenusSB method [Windows Shell], RemoveMenusSB method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_RemoveMenusSB, shell.IShellBrowser_RemoveMenusSB, shobjidl_core/IShellBrowser::RemoveMenusSB
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellBrowser.RemoveMenusSB
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellBrowser::RemoveMenusSB


## -description


Permits the container to remove any of its menu elements from the in-place composite menu and to free all associated resources.


## -parameters




### -param hmenuShared

Type: <b>HMENU</b>

A handle to the in-place composite menu that was constructed by calls to <a href="https://msdn.microsoft.com/62cbb593-7459-4a4f-96a2-3ec2287e6a26">IShellBrowser::InsertMenusSB</a> and the  <a href="https://msdn.microsoft.com/8ca7510a-e035-4ba2-98dd-57d777cae814">InsertMenu</a> function.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.




## -remarks



This method is similar to the <a href="https://msdn.microsoft.com/92d9fcda-8ede-4f38-ad56-59c4a75fe45a">IOleInPlaceFrame::RemoveMenus</a> method.

The object should always permit the container to remove its menu elements from the composite menu before deactivating the shared user interface.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
The method is called by the object application while it is being UI-deactivated so the browser can remove its menus.




## -see-also




<a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>
 

 

