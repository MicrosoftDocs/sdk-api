---
UID: NF:shlobj_core.Shell_GetImageLists
title: Shell_GetImageLists function (shlobj_core.h)
description: Retrieves system image lists for large and small icons.
helpviewer_keywords: ["Shell_GetImageLists","Shell_GetImageLists function [Windows Shell]","_win32_Shell_GetImageLists","shell.Shell_GetImageLists","shlobj_core/Shell_GetImageLists"]
old-location: shell\Shell_GetImageLists.htm
tech.root: shell
ms.assetid: c3b73616-849c-4149-b04d-a7d389ebf700
ms.date: 12/05/2018
ms.keywords: Shell_GetImageLists, Shell_GetImageLists function [Windows Shell], _win32_Shell_GetImageLists, shell.Shell_GetImageLists, shlobj_core/Shell_GetImageLists
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
 - Shell_GetImageLists
 - shlobj_core/Shell_GetImageLists
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
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - Shell_GetImageLists
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# Shell_GetImageLists function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Retrieves system image lists for large and small icons.

## -parameters

### -param phiml [in]

Type: <b>HIMAGELIST*</b>

A pointer to the handle of an image list which, on success, receives the system image list for large (32 x 32) icons.

### -param phimlSmall [in]

Type: <b>HIMAGELIST*</b>

A pointer to the handle of an image list which, on success, receives the system image list for small (16 x 16) icons.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> on success. On failure, returns <b>FALSE</b> and the image lists pointed to by <i>phiml</i> and <i>phimlSmall</i> are unchanged.

## -remarks

<div class="alert"><b>Important</b>  The image lists retrieved through this function are global system image lists; do not call <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_destroy">ImageList_Destroy</a> using them.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Controls/image-list-reference">Image Lists</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-shgetfileinfoa">SHGetFileInfo</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-shgetimagelist">SHGetImageList</a>
