---
UID: NF:shlobj.IDockingWindowFrame.FindToolbar
title: IDockingWindowFrame::FindToolbar
author: windows-sdk-content
description: Finds the specified IDockingWindow object in the toolbar frame and returns an interface pointer to it.
old-location: shell\IDockingWindowFrame_FindToolbar.htm
old-project: shell
ms.assetid: 9086f8ae-6a81-463d-9482-7a60701ab8de
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: FindToolbar, FindToolbar method [Windows Shell], FindToolbar method [Windows Shell],IDockingWindowFrame interface, IDockingWindowFrame interface [Windows Shell],FindToolbar method, IDockingWindowFrame.FindToolbar, IDockingWindowFrame::FindToolbar, _win32_IDockingWindowFrame_FindToolbar, shell.IDockingWindowFrame_FindToolbar, shlobj/IDockingWindowFrame::FindToolbar
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shlobj.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDockingWindowFrame.FindToolbar
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IDockingWindowFrame::FindToolbar


## -description


Finds the specified <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object in the toolbar frame and returns an interface pointer to it.


## -parameters




### -param pwszItem [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated, Unicode, application-defined string used to identify the object. This is the same string that was passed to the <a href="https://msdn.microsoft.com/b046bb62-8bc1-4021-bcb2-d4f23a9fccf4">AddToolbar</a> method.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired interface ID. This is typically IID_IDockingWindow.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a>. If an error occurs, this value receives a null pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d0dc10db-316a-4eaa-83db-3f186ee77071">IDockingWindowFrame</a>



<a href="https://msdn.microsoft.com/7418a6af-74ce-4435-8ed9-af106df0f95b">IDockingWindowSite</a>
 

 

