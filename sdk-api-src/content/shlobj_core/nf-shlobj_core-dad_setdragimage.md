---
UID: NF:shlobj_core.DAD_SetDragImage
title: DAD_SetDragImage function (shlobj_core.h)
description: Sets the drag image.
helpviewer_keywords: ["DAD_SetDragImage","DAD_SetDragImage function [Windows Shell]","shell.DAD_SetDragImage","shell_DAD_SetDragImage","shlobj_core/DAD_SetDragImage"]
old-location: shell\DAD_SetDragImage.htm
tech.root: shell
ms.assetid: 1e60e16c-3a12-48e2-a144-b3ba81599473
ms.date: 12/05/2018
ms.keywords: DAD_SetDragImage, DAD_SetDragImage function [Windows Shell], shell.DAD_SetDragImage, shell_DAD_SetDragImage, shlobj_core/DAD_SetDragImage
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
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DAD_SetDragImage
 - shlobj_core/DAD_SetDragImage
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
 - DAD_SetDragImage
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# DAD_SetDragImage function


## -description

<p class="CCE_Message">[<b>DAD_SetDragImage</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_begindrag">ImageList_BeginDrag</a> instead.]

Sets the drag image.

## -parameters

### -param him

Type: <b>HIMAGELIST</b>

A handle to an image list. This parameter uses the zero index in the ImageList.

### -param pptOffset

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to the coordinates used as the hot spot for dragging the image. The coordinates are relative to upper-left corner of the image.

## -returns

Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.

## -remarks

You can clear the drag image by setting the <i>him</i> parameter to <code>-1</code> and the <i>pptOffset</i> parameter to <code>NULL</code>. The image must have been set within the same thread.
