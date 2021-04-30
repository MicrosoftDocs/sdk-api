---
UID: NF:commctrl.InitializeFlatSB
title: InitializeFlatSB function (commctrl.h)
description: Initializes flat scroll bars for a particular window.
helpviewer_keywords: ["InitializeFlatSB","InitializeFlatSB function [Windows Controls]","_win32_InitializeFlatSB","_win32_InitializeFlatSB_cpp","commctrl/InitializeFlatSB","controls.InitializeFlatSB","controls._win32_InitializeFlatSB"]
old-location: controls\InitializeFlatSB.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\initializeflatsb.htm
ms.date: 12/05/2018
ms.keywords: InitializeFlatSB, InitializeFlatSB function [Windows Controls], _win32_InitializeFlatSB, _win32_InitializeFlatSB_cpp, commctrl/InitializeFlatSB, controls.InitializeFlatSB, controls._win32_InitializeFlatSB
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitializeFlatSB
 - commctrl/InitializeFlatSB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - InitializeFlatSB
---

# InitializeFlatSB function


## -description

Initializes flat scroll bars for a particular window.

## -parameters

### -param unnamedParam1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that will receive flat scroll bars.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.

## -remarks

This function must be called before any other flat scroll bar functions are called. The window will receive flat scroll bars by default. The scroll bar style can be changed with the <a href="/windows/desktop/api/commctrl/nf-commctrl-flatsb_setscrollprop">FlatSB_SetScrollProp</a> function. 

<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>