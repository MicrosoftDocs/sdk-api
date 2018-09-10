---
UID: NF:commctrl.InitMUILanguage
title: InitMUILanguage function
author: windows-sdk-content
description: Enables an application to specify a language to be used with the common controls that is different from the system language.
old-location: controls\InitMUILanguage.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\initmuilanguage.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InitMUILanguage, InitMUILanguage function [Windows Controls], _win32_InitMUILanguage, _win32_InitMUILanguage_cpp, commctrl/InitMUILanguage, controls.InitMUILanguage, controls._win32_InitMUILanguage
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
 - InitMUILanguage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitMUILanguage function


## -description


Enables an application to specify a language to be used with the common controls that is different from the system language. 


## -parameters




### -param uiLang

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LANGID</a></b>

The  <a href="https://msdn.microsoft.com/en-us/library/Dd318691(v=VS.85).aspx">language identifier</a> of the language to be used by the common controls. 


## -returns



None




## -remarks



This function enables an application to override the system language setting, and specify a different language for the common controls. The selected language only applies to the process that <b>InitMUILanguage</b> is called from. See <a href="https://msdn.microsoft.com/en-us/library/Dd318661(v=VS.85).aspx">Internationalization for Windows Applications</a> for further discussion of localization.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775676(v=VS.85).aspx">GetMUILanguage</a>
 

 

