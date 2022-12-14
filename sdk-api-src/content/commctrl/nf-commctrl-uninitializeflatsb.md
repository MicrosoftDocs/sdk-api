---
UID: NF:commctrl.UninitializeFlatSB
title: UninitializeFlatSB function (commctrl.h)
description: Uninitializes flat scroll bars for a particular window. The specified window will revert to standard scroll bars.
helpviewer_keywords: ["UninitializeFlatSB","UninitializeFlatSB function [Windows Controls]","_win32_UninitializeFlatSB","_win32_UninitializeFlatSB_cpp","commctrl/UninitializeFlatSB","controls.UninitializeFlatSB","controls._win32_UninitializeFlatSB"]
old-location: controls\UninitializeFlatSB.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\uninitializeflatsb.htm
ms.date: 12/05/2018
ms.keywords: UninitializeFlatSB, UninitializeFlatSB function [Windows Controls], _win32_UninitializeFlatSB, _win32_UninitializeFlatSB_cpp, commctrl/UninitializeFlatSB, controls.UninitializeFlatSB, controls._win32_UninitializeFlatSB
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
 - UninitializeFlatSB
 - commctrl/UninitializeFlatSB
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
 - UninitializeFlatSB
---

# UninitializeFlatSB function


## -description

Uninitializes flat scroll bars for a particular window. The specified window will revert to standard scroll bars.

## -parameters

### -param unnamedParam1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window with the flat scroll bars that will be uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the following values. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
One of the window's scroll bars is currently in use. The operation cannot be completed at this time. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The window does not have flat scroll bars initialized. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful. 

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>