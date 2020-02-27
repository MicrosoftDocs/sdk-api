---
UID: NF:commctrl.GetMUILanguage
title: GetMUILanguage function (commctrl.h)
description: Gets the language currently in use by the common controls for a particular process.
old-location: controls\GetMUILanguage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\getmuilanguage.htm
ms.date: 12/05/2018
ms.keywords: GetMUILanguage, GetMUILanguage function [Windows Controls], _win32_GetMUILanguage, _win32_GetMUILanguage_cpp, commctrl/GetMUILanguage, controls.GetMUILanguage, controls._win32_GetMUILanguage
f1_keywords:
- commctrl/GetMUILanguage
dev_langs:
- c++
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
req.dll: Comctl32.dll (version 5.80 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Comctl32.dll
api_name:
- GetMUILanguage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMUILanguage function


## -description


Gets the language currently in use by the common controls for a particular process. 


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LANGID</a></b>

Returns the <a href="https://docs.microsoft.com/windows/desktop/Intl/language-identifiers">language identifier</a> of the language an application has specified for the common controls by calling <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-initmuilanguage">InitMUILanguage</a>. <b>GetMUILanguage</b> returns the value for the process from which it is called. If 
						<b>InitMUILanguage</b> has not been called or was not called from the same process, <b>GetMUILanguage</b> returns the language-neutral LANGID, <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>(LANG_NEUTRAL, SUBLANG_NEUTRAL).




## -remarks



See <a href="https://docs.microsoft.com/windows/desktop/Intl/international-support">Internationalization for Windows Applications</a> for further discussion of localization.



