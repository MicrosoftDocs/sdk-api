---
UID: NF:commctrl.GetMUILanguage
title: GetMUILanguage function
author: windows-sdk-content
description: Gets the language currently in use by the common controls for a particular process.
old-location: controls\GetMUILanguage.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\functions\getmuilanguage.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetMUILanguage, GetMUILanguage function [Windows Controls], _win32_GetMUILanguage, _win32_GetMUILanguage_cpp, commctrl/GetMUILanguage, controls.GetMUILanguage, controls._win32_GetMUILanguage
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
 - GetMUILanguage
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 5.80 or later)
req.irql: 
---

# GetMUILanguage function


## -description


Gets the language currently in use by the common controls for a particular process. 


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LANGID</a></b>

Returns the <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> of the language an application has specified for the common controls by calling <a href="https://msdn.microsoft.com/library/Bb775699(v=VS.85).aspx">InitMUILanguage</a>. <b>GetMUILanguage</b> returns the value for the process from which it is called. If 
						<b>InitMUILanguage</b> has not been called or was not called from the same process, <b>GetMUILanguage</b> returns the language-neutral LANGID, <a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>(LANG_NEUTRAL, SUBLANG_NEUTRAL).




## -remarks



See <a href="https://msdn.microsoft.com/90dbbd70-3609-4c12-bdc1-7fa222c96f67">Internationalization for Windows Applications</a> for further discussion of localization.



