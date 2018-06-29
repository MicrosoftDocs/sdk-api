---
UID: NF:commctrl.InitCommonControls
title: InitCommonControls function
author: windows-sdk-content
description: Registers and initializes certain common control window classes. This function is obsolete. New applications should use the InitCommonControlsEx function.
old-location: controls\InitCommonControls.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\functions\initcommoncontrols.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: InitCommonControls, InitCommonControls function [Windows Controls], _win32_InitCommonControls, _win32_InitCommonControls_cpp, commctrl/InitCommonControls, controls.InitCommonControls, controls._win32_InitCommonControls
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
 - Ext-MS-Win-Shell-ComCtl32-Init-l1-1-0.dll
 - Ext-MS-Win-Shell-ComCtl32-Init-L1-1-1.dll
api_name:
 - InitCommonControls
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# InitCommonControls function


## -description


Registers and initializes certain common control window classes. This function is obsolete. New applications should use the <a href="https://msdn.microsoft.com/library/Bb775697(v=VS.85).aspx">InitCommonControlsEx</a> function. 


## -parameters






## -returns



This function does not return a value.




## -remarks



Under Comctl32.dll version 5.x, only Windows 95 classes (ICC_WIN95_CLASSES) can be registered through <b>InitCommonControls</b>. Programs which require additional common control classes must use the <a href="https://msdn.microsoft.com/library/Bb775697(v=VS.85).aspx">InitCommonControlsEx</a> function.

Under Comctl32.dll version 6.0 and later, <b>InitCommonControls</b> does nothing. Applications must explicitly register all common controls through <a href="https://msdn.microsoft.com/library/Bb775697(v=VS.85).aspx">InitCommonControlsEx</a>.



