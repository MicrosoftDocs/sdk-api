---
UID: NF:shlobj.IFileViewerSite.GetPinnedWindow
title: IFileViewerSite::GetPinnedWindow
author: windows-sdk-content
description: Gets the handle to the current pinned window, if one exists.
old-location: shell\IFileViewerSite_GetPinnedWindow.htm
old-project: shell
ms.assetid: ef5b4668-1e74-42c2-903e-8d4cf5e2f74e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPinnedWindow, GetPinnedWindow method [Windows Shell], GetPinnedWindow method [Windows Shell],IFileViewerSite interface, IFileViewerSite interface [Windows Shell],GetPinnedWindow method, IFileViewerSite.GetPinnedWindow, IFileViewerSite::GetPinnedWindow, _win32_IFileViewerSite_GetPinnedWindow, shell.IFileViewerSite_GetPinnedWindow, shlobj/IFileViewerSite::GetPinnedWindow
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
 - IFileViewerSite.GetPinnedWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IFileViewerSite::GetPinnedWindow


## -description


Gets the handle to the current pinned window, if one exists.


## -parameters




### -param phwnd [out]

Type: <b>HWND*</b>

A pointer to the handle of the current pinned window or <b>NULL</b> if no pinned window exists.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/500fa3e4-1865-4543-ae34-8bd7ce9d94cb">IFileViewerSite</a>
 

 

