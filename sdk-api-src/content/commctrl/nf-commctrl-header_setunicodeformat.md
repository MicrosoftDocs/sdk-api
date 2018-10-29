---
UID: NF:commctrl.Header_SetUnicodeFormat
title: Header_SetUnicodeFormat macro
author: windows-sdk-content
description: Sets the UNICODE character format flag for the control.
old-location: controls\Header_SetUnicodeFormat.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setunicodeformat.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Header_SetUnicodeFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Header_SetUnicodeFormat macro


## -description


Sets the UNICODE character format flag for the control. This message allows you to change the character set used by the control at run time rather than having to re-create the control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775371(v=VS.85).aspx">HDM_SETUNICODEFORMAT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the control. 


### -param fUnicode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Determines the character set that is used by the control. If this value is nonzero, the control will use Unicode characters. If this value is zero, the control will use ANSI characters. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775405(v=VS.85).aspx">Header_GetUnicodeFormat</a>
 

 

