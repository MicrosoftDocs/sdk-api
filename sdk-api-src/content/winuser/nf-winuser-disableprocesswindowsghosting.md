---
UID: NF:winuser.DisableProcessWindowsGhosting
title: DisableProcessWindowsGhosting function (winuser.h)
description: Disables the window ghosting feature for the calling GUI process. Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.
old-location: winprog\disableprocesswindowsghosting.htm
tech.root: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtldisableprocesswindowsghosting.htm
ms.date: 12/05/2018
ms.keywords: DisableProcessWindowsGhosting, DisableProcessWindowsGhosting function [Windows API], winprog.disableprocesswindowsghosting, winui.disableprocesswindowsghosting, winuser/DisableProcessWindowsGhosting
f1_keywords:
- winuser/DisableProcessWindowsGhosting
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
api_name:
- DisableProcessWindowsGhosting
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DisableProcessWindowsGhosting function


## -description


Disables the window ghosting feature for the calling GUI process. Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.


## -parameters






## -remarks



After calling <b>DisableProcessWindowsGhosting</b>, the ghosting feature is disabled for the duration of the process.


		



