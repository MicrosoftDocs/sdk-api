---
UID: NF:commctrl.InitializeFlatSB
title: InitializeFlatSB function
author: windows-sdk-content
description: Initializes flat scroll bars for a particular window.
old-location: controls\InitializeFlatSB.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\initializeflatsb.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: InitializeFlatSB, InitializeFlatSB function [Windows Controls], _win32_InitializeFlatSB, _win32_InitializeFlatSB_cpp, commctrl/InitializeFlatSB, controls.InitializeFlatSB, controls._win32_InitializeFlatSB
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - InitializeFlatSB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- InitializeFlatSB
: 
---

# InitializeFlatSB function


## -description


Initializes flat scroll bars for a particular window. 


## -parameters




### -param Arg1

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the window that will receive flat scroll bars. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.




## -remarks



This function must be called before any other flat scroll bar functions are called. The window will receive flat scroll bars by default. The scroll bar style can be changed with the <a href="https://msdn.microsoft.com/en-us/library/Bb775438(v=VS.85).aspx">FlatSB_SetScrollProp</a> function. 

<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>


