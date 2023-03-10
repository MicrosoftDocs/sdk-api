---
UID: NF:shellapi.DragAcceptFiles
title: DragAcceptFiles function (shellapi.h)
description: Registers whether a window accepts dropped files.
helpviewer_keywords: ["DragAcceptFiles","DragAcceptFiles function [Windows Shell]","_win32_DragAcceptFiles","shell.DragAcceptFiles","shellapi/DragAcceptFiles"]
old-location: shell\DragAcceptFiles.htm
tech.root: shell
ms.assetid: 1f16f6e4-7847-4bc7-adce-995876db24bd
ms.date: 12/05/2018
ms.keywords: DragAcceptFiles, DragAcceptFiles function [Windows Shell], _win32_DragAcceptFiles, shell.DragAcceptFiles, shellapi/DragAcceptFiles
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
 - DragAcceptFiles
 - shellapi/DragAcceptFiles
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
 - DragAcceptFiles
---

# DragAcceptFiles function


## -description

Registers whether a window accepts dropped files.

## -parameters

### -param hWnd

Type: <b>HWND</b>

The identifier of the window that is registering whether it will accept dropped files.

### -param fAccept

Type: <b>BOOL</b>

A value that indicates if the window identified by the <i>hWnd</i> parameter accepts dropped files. This value is <b>TRUE</b> to accept dropped files or <b>FALSE</b> to discontinue accepting dropped files.

## -remarks

An application that calls <b>DragAcceptFiles</b> with the <i>fAccept</i> parameter set to <b>TRUE</b> has identified itself as able to process the <a href="/windows/desktop/shell/wm-dropfiles">WM_DROPFILES</a> message from File Manager.