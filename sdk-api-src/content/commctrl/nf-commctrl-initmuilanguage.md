---
UID: NF:commctrl.InitMUILanguage
title: InitMUILanguage function
author: windows-sdk-content
description: Enables an application to specify a language to be used with the common controls that is different from the system language.
old-location: controls\InitMUILanguage.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\initmuilanguage.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InitMUILanguage, InitMUILanguage function [Windows Controls], _win32_InitMUILanguage, _win32_InitMUILanguage_cpp, commctrl/InitMUILanguage, controls.InitMUILanguage, controls._win32_InitMUILanguage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.redist: 
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
 - InitMUILanguage
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 5.80 or later)
req.irql: 
---

# InitMUILanguage function


## -description


Enables an application to specify a language to be used with the common controls that is different from the system language. 


## -parameters




### -param uiLang

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LANGID</a></b>

The  <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">language identifier</a> of the language to be used by the common controls. 


## -returns



None




## -remarks



This function enables an application to override the system language setting, and specify a different language for the common controls. The selected language only applies to the process that <b>InitMUILanguage</b> is called from. See <a href="https://msdn.microsoft.com/90dbbd70-3609-4c12-bdc1-7fa222c96f67">Internationalization for Windows Applications</a> for further discussion of localization.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775676(v=VS.85).aspx">GetMUILanguage</a>
 

 

