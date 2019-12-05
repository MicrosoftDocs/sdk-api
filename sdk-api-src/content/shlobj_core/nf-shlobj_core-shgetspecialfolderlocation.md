---
UID: NF:shlobj_core.SHGetSpecialFolderLocation
title: SHGetSpecialFolderLocation function (shlobj_core.h)
description: SHGetSpecialFolderLocation is not supported and may be altered or unavailable in the future. Instead, use SHGetFolderLocation.
old-location: shell\SHGetSpecialFolderLocation.htm
tech.root: shell
ms.assetid: 10b00497-fc3b-4e34-acd8-bc0721c0dc05
ms.date: 12/05/2018
ms.keywords: SHGetSpecialFolderLocation, SHGetSpecialFolderLocation function [Windows Shell], _win32_SHGetSpecialFolderLocation, _win32_SHGetSpecialFolderLocation_cpp, shell.SHGetSpecialFolderLocation, shlobj_core/SHGetSpecialFolderLocation
ms.topic: function
f1_keywords:
- shlobj_core/SHGetSpecialFolderLocation
dev_langs:
- c++
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shell32.dll
- ext-ms-win-shell-shell32-l1-2-1.dll
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
- Windows.Storage.dll
- Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
- SHGetSpecialFolderLocation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHGetSpecialFolderLocation function


## -description


<p class="CCE_Message">[<b>SHGetSpecialFolderLocation</b> is not supported and may be altered or unavailable in the future. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation">SHGetFolderLocation</a>.]

Retrieves a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure of a special folder.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

Reserved.


### -param csidl [in]

Type: <b>int</b>

A <a href="https://docs.microsoft.com/windows/desktop/shell/csidl">CSIDL</a> value that identifies the folder of interest.


### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

A PIDL specifying the folder's location relative to the root of the namespace (the desktop). It is the responsibility of the calling application to free the returned IDList by using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha">SHGetSpecialFolderPath</a>
 

 

