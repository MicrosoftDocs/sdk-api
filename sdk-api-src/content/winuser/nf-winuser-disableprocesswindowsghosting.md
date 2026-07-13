---
UID: NF:winuser.DisableProcessWindowsGhosting
title: DisableProcessWindowsGhosting function (winuser.h)
description: Disables the window ghosting feature for the calling GUI process. Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.
helpviewer_keywords: ["DisableProcessWindowsGhosting","DisableProcessWindowsGhosting function [Windows API]","winprog.disableprocesswindowsghosting","winui.disableprocesswindowsghosting","winuser/DisableProcessWindowsGhosting"]
old-location: winprog\disableprocesswindowsghosting.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtldisableprocesswindowsghosting.htm
ms.date: 12/05/2018
ms.keywords: DisableProcessWindowsGhosting, DisableProcessWindowsGhosting function [Windows API], winprog.disableprocesswindowsghosting, winui.disableprocesswindowsghosting, winuser/DisableProcessWindowsGhosting
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DisableProcessWindowsGhosting
 - winuser/DisableProcessWindowsGhosting
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
api_name:
 - DisableProcessWindowsGhosting
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# DisableProcessWindowsGhosting function


## -description

Disables the window ghosting feature for the calling GUI process. Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.



## -remarks

After calling <b>DisableProcessWindowsGhosting</b>, the ghosting feature is disabled for the duration of the process.

