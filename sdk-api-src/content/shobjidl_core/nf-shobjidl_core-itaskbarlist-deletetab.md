---
UID: NF:shobjidl_core.ITaskbarList.DeleteTab
title: ITaskbarList::DeleteTab
author: windows-sdk-content
description: Deletes an item from the taskbar.
old-location: shell\ITaskbarList_DeleteTab.htm
tech.root: shell
ms.assetid: bf1b3d27-5cd3-44c8-81e6-d9418d30ffe3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteTab, DeleteTab method [Windows Shell], DeleteTab method [Windows Shell],ITaskbarList interface, ITaskbarList interface [Windows Shell],DeleteTab method, ITaskbarList.DeleteTab, ITaskbarList::DeleteTab, _win32_ITaskbarList_DeleteTab, shell.ITaskbarList_DeleteTab, shobjidl_core/ITaskbarList::DeleteTab
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ITaskbarList.DeleteTab
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskbarList::DeleteTab


## -description


Deletes an item from the taskbar.


## -parameters




### -param hwnd

Type: <b>HWND</b>

A handle to the window to be deleted from the taskbar.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



