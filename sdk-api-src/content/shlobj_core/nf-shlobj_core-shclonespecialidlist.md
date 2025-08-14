---
UID: NF:shlobj_core.SHCloneSpecialIDList
title: SHCloneSpecialIDList function (shlobj_core.h)
description: SHCloneSpecialIDList may be altered or unavailable. Instead, use SHGetSpecialFolderLocation.
helpviewer_keywords: ["SHCloneSpecialIDList","SHCloneSpecialIDList function [Windows Shell]","_win32_SHCloneSpecialIDList","shell.SHCloneSpecialIDList","shlobj_core/SHCloneSpecialIDList"]
old-location: shell\SHCloneSpecialIDList.htm
tech.root: shell
ms.assetid: ef8a6168-c495-47a7-af97-dfee19a41f64
ms.date: 12/05/2018
ms.keywords: SHCloneSpecialIDList, SHCloneSpecialIDList function [Windows Shell], _win32_SHCloneSpecialIDList, shell.SHCloneSpecialIDList, shlobj_core/SHCloneSpecialIDList
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCloneSpecialIDList
 - shlobj_core/SHCloneSpecialIDList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
api_name:
 - SHCloneSpecialIDList
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# SHCloneSpecialIDList function


## -description

<p class="CCE_Message">[<b>SHCloneSpecialIDList</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation">SHGetSpecialFolderLocation</a>.]

Retrieves a pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that specifies a special folder.

## -parameters

### -param hwnd

Type: <b>HWND</b>

Reserved.

### -param csidl [in]

Type: <b>int</b>

A <a href="/windows/desktop/shell/csidl">CSIDL</a> value that identifies the folder of interest.

### -param fCreate [in]

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates if the folder should be created if it does not already exist. If  <i>fCreate</i> is <b>TRUE</b>, the folder is created. If it is <b>FALSE</b>, the folder is not created.

## -returns

Type: <b>PIDLIST_ABSOLUTE</b>

Returns a pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure of a special folder specified by <i>csidl</i>. The function creates the folder if <i>fCreate</i> is <b>TRUE</b>.

## -remarks

When finished, you should free the pointer to the cloned folder with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a>.
