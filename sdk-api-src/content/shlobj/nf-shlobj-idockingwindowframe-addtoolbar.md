---
UID: NF:shlobj.IDockingWindowFrame.AddToolbar
title: IDockingWindowFrame::AddToolbar
author: windows-sdk-content
description: Adds the specified IDockingWindow object to the frame.
old-location: shell\IDockingWindowFrame_AddToolbar.htm
tech.root: shell
ms.assetid: b046bb62-8bc1-4021-bcb2-d4f23a9fccf4
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: 0, AddToolbar, AddToolbar method [Windows Shell], AddToolbar method [Windows Shell],IDockingWindowFrame interface, DWFAF_AUTOHIDE, DWFAF_GROUP1, DWFAF_GROUP2, DWFAF_HIDDEN, IDockingWindowFrame interface [Windows Shell],AddToolbar method, IDockingWindowFrame.AddToolbar, IDockingWindowFrame::AddToolbar, _win32_IDockingWindowFrame_AddToolbar, shell.IDockingWindowFrame_AddToolbar, shlobj/IDockingWindowFrame::AddToolbar
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj.h
req.include-header: 
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
 - IDockingWindowFrame.AddToolbar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDockingWindowFrame::AddToolbar


## -description


Adds the specified <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object to the frame.


## -parameters




### -param punkSrc [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object to be added.


### -param pwszItem [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated, Unicode, application-defined string that is used to identify the docking window object.


### -param dwAddFlags

Type: <b>DWORD</b>

Flags that apply to the docking window object that is being added. One or more of the following values.



#### 0

The docking window is a regular, visible docking window.



#### DWFAF_HIDDEN (0x0001)

The docking window is added but is not shown. To show it at a later time, call its <a href="https://msdn.microsoft.com/c33031d4-f9f4-4210-93be-963e5f299408">IDockingWindow::ShowDW</a> method.



#### DWFAF_GROUP1 (0x0002)

Reserved. Do not use.



#### DWFAF_GROUP2 (0x0004)

Reserved. Do not use.



#### DWFAF_AUTOHIDE (0x0010)

Reserved. Do not use.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d0dc10db-316a-4eaa-83db-3f186ee77071">IDockingWindowFrame</a>



<a href="https://msdn.microsoft.com/7418a6af-74ce-4435-8ed9-af106df0f95b">IDockingWindowSite</a>
 

 

