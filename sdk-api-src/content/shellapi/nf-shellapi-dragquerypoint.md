---
UID: NF:shellapi.DragQueryPoint
title: DragQueryPoint function (shellapi.h)
description: Retrieves the position of the mouse pointer at the time a file was dropped during a drag-and-drop operation.
helpviewer_keywords: ["DragQueryPoint","DragQueryPoint function [Windows Shell]","_win32_DragQueryPoint","shell.DragQueryPoint","shellapi/DragQueryPoint"]
old-location: shell\DragQueryPoint.htm
tech.root: shell
ms.assetid: 87794ab0-a075-4a1f-869f-5998bdc57a1d
ms.date: 12/05/2018
ms.keywords: DragQueryPoint, DragQueryPoint function [Windows Shell], _win32_DragQueryPoint, shell.DragQueryPoint, shellapi/DragQueryPoint
req.header: shellapi.h
req.include-header: 
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DragQueryPoint
 - shellapi/DragQueryPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - DragQueryPoint
---

# DragQueryPoint function


## -description

Retrieves the position of the mouse pointer at the time a file was dropped during a drag-and-drop operation.

## -parameters

### -param hDrop [in]

Type: <b>HDROP</b>

Handle of the drop structure that describes the dropped file.

### -param ppt [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

Pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that, when this function returns successfully, receives the coordinates of the mouse pointer at the time the file was dropped.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the drop occurred in the client area of the window; otherwise <b>FALSE</b>.

## -remarks

The window for which coordinates are returned is the window that received the <a href="/windows/desktop/shell/wm-dropfiles">WM_DROPFILES</a> message.

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-dragqueryfilea">DragQueryFile</a>