---
UID: NF:shlobj.IFileViewerSite.SetPinnedWindow
title: IFileViewerSite::SetPinnedWindow
author: windows-sdk-content
description: Sets the pinned window. When the user selects a new file to view, the Shell directs the file viewer to display the new file in the pinned window instead of creating a new window.
old-location: shell\IFileViewerSite_SetPinnedWindow.htm
old-project: shell
ms.assetid: 7c2bcb76-84aa-404e-9e0a-9ee966b6c91e
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IFileViewerSite interface [Windows Shell],SetPinnedWindow method, IFileViewerSite.SetPinnedWindow, IFileViewerSite::SetPinnedWindow, SetPinnedWindow, SetPinnedWindow method [Windows Shell], SetPinnedWindow method [Windows Shell],IFileViewerSite interface, _win32_IFileViewerSite_SetPinnedWindow, shell.IFileViewerSite_SetPinnedWindow, shlobj/IFileViewerSite::SetPinnedWindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shlobj.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IFileViewerSite.SetPinnedWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IFileViewerSite::SetPinnedWindow


## -description


Sets the pinned window. When the user selects a new file to view, the Shell directs the file viewer to display the new file in the pinned window instead of creating a new window.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the new pinned window or <b>NULL</b> if there is to be no pinned window.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/500fa3e4-1865-4543-ae34-8bd7ce9d94cb">IFileViewerSite</a>
 

 

