---
UID: NF:shlobj.IDockingWindowFrame.RemoveToolbar
title: IDockingWindowFrame::RemoveToolbar
author: windows-sdk-content
description: Removes the specified IDockingWindow from the toolbar frame.
old-location: shell\IDockingWindowFrame_RemoveToolbar.htm
old-project: shell
ms.assetid: 4ebc4561-a7fe-4fa4-ae2a-88030ede02e7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DWFRF_DELETECONFIGDATA, DWFRF_NORMAL, IDockingWindowFrame interface [Windows Shell],RemoveToolbar method, IDockingWindowFrame.RemoveToolbar, IDockingWindowFrame::RemoveToolbar, RemoveToolbar, RemoveToolbar method [Windows Shell], RemoveToolbar method [Windows Shell],IDockingWindowFrame interface, _win32_IDockingWindowFrame_RemoveToolbar, shell.IDockingWindowFrame_RemoveToolbar, shlobj/IDockingWindowFrame::RemoveToolbar
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
 - IDockingWindowFrame.RemoveToolbar
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IDockingWindowFrame::RemoveToolbar


## -description


Removes the specified <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> from the toolbar frame.


## -parameters




### -param punkSrc [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object to be removed. The <a href="https://msdn.microsoft.com/d0dc10db-316a-4eaa-83db-3f186ee77071">IDockingWindowFrame</a> implementation calls the <a href="https://msdn.microsoft.com/29e57436-cc8f-46e8-bc1a-b44bd803c4a8">IDockingWindow::CloseDW</a> and <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IDockingWindow::Release</a> methods.


### -param dwRemoveFlags

Type: <b>DWORD</b>

Option flags for removing the docking window object. This parameter can be one or more of the following values:



#### DWFRF_NORMAL (0x0000)

The default delete processing is performed.



#### DWFRF_DELETECONFIGDATA (0x0001)

In addition to deleting the toolbar, any configuration data is removed as well.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d0dc10db-316a-4eaa-83db-3f186ee77071">IDockingWindowFrame</a>



<a href="https://msdn.microsoft.com/7418a6af-74ce-4435-8ed9-af106df0f95b">IDockingWindowSite</a>
 

 

