---
UID: NF:commctrl.Header_SetUnicodeFormat
title: Header_SetUnicodeFormat macro
author: windows-driver-content
description: Sets the UNICODE character format flag for the control.
old-location: controls\Header_SetUnicodeFormat.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setunicodeformat.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Header_SetUnicodeFormat, Header_SetUnicodeFormat macro [Windows Controls], _win32_Header_SetUnicodeFormat, _win32_Header_SetUnicodeFormat_cpp, commctrl/Header_SetUnicodeFormat, controls.Header_SetUnicodeFormat, controls._win32_Header_SetUnicodeFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	Header_SetUnicodeFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Header_SetUnicodeFormat macro


## -description


Sets the UNICODE character format flag for the control. This message allows you to change the character set used by the control at run time rather than having to re-create the control. You can use this macro or send the <a href="https://msdn.microsoft.com/18161fe5-c779-4be0-9e7a-1b5948e42b80">HDM_SETUNICODEFORMAT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control. 


### -param fUnicode

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Determines the character set that is used by the control. If this value is nonzero, the control will use Unicode characters. If this value is zero, the control will use ANSI characters. 


## -see-also




<a href="https://msdn.microsoft.com/5485c16e-a709-4195-89d7-bb30fad0ec5d">Header_GetUnicodeFormat</a>
 

 

