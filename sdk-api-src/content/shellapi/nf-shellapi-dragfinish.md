---
UID: NF:shellapi.DragFinish
title: DragFinish function (shellapi.h)
description: Releases memory that the system allocated for use in transferring file names to the application.
old-location: shell\DragFinish.htm
tech.root: shell
ms.assetid: 9b15e8a5-de68-4dcb-8e1a-0ee0393aa9db
ms.date: 12/05/2018
ms.keywords: DragFinish, DragFinish function [Windows Shell], _win32_DragFinish, shell.DragFinish, shellapi/DragFinish
ms.topic: function
f1_keywords:
- shellapi/DragFinish
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shell32.dll
api_name:
- DragFinish
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DragFinish function


## -description


Releases memory that the system allocated for use in transferring file names to the application.


## -parameters




### -param hDrop

Type: <b>HDROP</b>

Identifier of the structure that describes dropped files. This handle is retrieved from the <i>wParam</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/shell/wm-dropfiles">WM_DROPFILES</a> message.


## -returns



No return value.



