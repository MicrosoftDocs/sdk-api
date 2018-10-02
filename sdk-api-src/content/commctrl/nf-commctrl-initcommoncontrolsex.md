---
UID: NF:commctrl.InitCommonControlsEx
title: InitCommonControlsEx function
author: windows-sdk-content
description: Ensures that the common control DLL (Comctl32.dll) is loaded, and registers specific common control classes from the DLL. An application must call this function before creating a common control.
old-location: controls\InitCommonControlsEx.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\initcommoncontrolsex.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: InitCommonControlsEx, InitCommonControlsEx function [Windows Controls], _win32_InitCommonControlsEx, _win32_InitCommonControlsEx_cpp, commctrl/InitCommonControlsEx, controls.InitCommonControlsEx, controls._win32_InitCommonControlsEx
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
req.dll: Comctl32.dll (version 4.70 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
 - Ext-MS-Win-Shell-ComCtl32-Init-l1-1-0.dll
 - Ext-MS-Win-Shell-ComCtl32-Init-L1-1-1.dll
api_name:
 - InitCommonControlsEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitCommonControlsEx function


## -description


Ensures that the common control DLL (Comctl32.dll) is loaded, and registers specific common control classes from the  DLL. An application must call this function before creating a common control. 


## -parameters




### -param picce [in]

Type: <b>const LPINITCOMMONCONTROLSEX</b>

A pointer to an <a href="https://msdn.microsoft.com/ad5a1cec-deaf-4011-9313-e79c13e37ce4">INITCOMMONCONTROLSEX</a> structure that contains information specifying which control classes will be registered. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. 




## -remarks



The effect of each call to <b>InitCommonControlsEx</b> is cumulative. For example, if <b>InitCommonControlsEx</b> is called with the <a href="https://msdn.microsoft.com/ad5a1cec-deaf-4011-9313-e79c13e37ce4">ICC_UPDOWN_CLASS</a> flag, then is later called with the <a href="https://msdn.microsoft.com/ad5a1cec-deaf-4011-9313-e79c13e37ce4">ICC_HOTKEY_CLASS</a> flag, the result is that both the up-down and hot key common control classes are registered and available to the application.
			



