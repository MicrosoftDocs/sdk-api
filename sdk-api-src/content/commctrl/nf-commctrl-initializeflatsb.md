---
UID: NF:commctrl.InitializeFlatSB
title: InitializeFlatSB function
author: windows-sdk-content
description: Initializes flat scroll bars for a particular window.
old-location: controls\InitializeFlatSB.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\initializeflatsb.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: InitializeFlatSB, InitializeFlatSB function [Windows Controls], _win32_InitializeFlatSB, _win32_InitializeFlatSB_cpp, commctrl/InitializeFlatSB, controls.InitializeFlatSB, controls._win32_InitializeFlatSB
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 4.71 or later)
req.irql: 
---

# InitializeFlatSB function


## -description


Initializes flat scroll bars for a particular window. 


## -parameters




### -param Arg1

TBD




#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window that will receive flat scroll bars. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.




## -remarks



This function must be called before any other flat scroll bar functions are called. The window will receive flat scroll bars by default. The scroll bar style can be changed with the <a href="https://msdn.microsoft.com/f9779369-2416-499d-a20b-a2fc190e4e01">FlatSB_SetScrollProp</a> function. 

<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>


