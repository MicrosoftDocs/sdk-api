---
UID: NF:commctrl.InitMUILanguage
title: InitMUILanguage function (commctrl.h)
description: Enables an application to specify a language to be used with the common controls that is different from the system language.
helpviewer_keywords: ["InitMUILanguage","InitMUILanguage function [Windows Controls]","_win32_InitMUILanguage","_win32_InitMUILanguage_cpp","commctrl/InitMUILanguage","controls.InitMUILanguage","controls._win32_InitMUILanguage"]
old-location: controls\InitMUILanguage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\initmuilanguage.htm
ms.date: 12/05/2018
ms.keywords: InitMUILanguage, InitMUILanguage function [Windows Controls], _win32_InitMUILanguage, _win32_InitMUILanguage_cpp, commctrl/InitMUILanguage, controls.InitMUILanguage, controls._win32_InitMUILanguage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitMUILanguage
 - commctrl/InitMUILanguage
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
 - InitMUILanguage
---

# InitMUILanguage function


## -description

Enables an application to specify a language to be used with the common controls that is different from the system language.

## -parameters

### -param uiLang

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LANGID</a></b>

The  <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> of the language to be used by the common controls.

## -remarks

This function enables an application to override the system language setting, and specify a different language for the common controls. The selected language only applies to the process that <b>InitMUILanguage</b> is called from. See <a href="/windows/desktop/Intl/international-support">Internationalization for Windows Applications</a> for further discussion of localization.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-getmuilanguage">GetMUILanguage</a>