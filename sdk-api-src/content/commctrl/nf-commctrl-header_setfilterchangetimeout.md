---
UID: NF:commctrl.Header_SetFilterChangeTimeout
title: Header_SetFilterChangeTimeout macro
author: windows-sdk-content
description: Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an HDN_FILTERCHANGE notification. You can use this macro or send the HDM_SETFILTERCHANGETIMEOUT message explicitly.
old-location: controls\Header_SetFilterChangeTimeout.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setfilterchangetimeout.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Header_SetFilterChangeTimeout, Header_SetFilterChangeTimeout macro [Windows Controls], _win32_Header_SetFilterChangeTimeout, _win32_Header_SetFilterChangeTimeout_cpp, commctrl/Header_SetFilterChangeTimeout, controls.Header_SetFilterChangeTimeout, controls._win32_Header_SetFilterChangeTimeout
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Header_SetFilterChangeTimeout
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Header_SetFilterChangeTimeout macro


## -description


Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an <a href="https://msdn.microsoft.com/library/Bb775277(v=VS.85).aspx">HDN_FILTERCHANGE</a> notification. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb775359(v=VS.85).aspx">HDM_SETFILTERCHANGETIMEOUT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


### -param i

Type: <b>int</b>

The timeout value, in milliseconds. 


## -see-also




<a href="https://msdn.microsoft.com/library/Bb775359(v=VS.85).aspx">HDM_SETFILTERCHANGETIMEOUT</a>



<a href="https://msdn.microsoft.com/library/Bb775277(v=VS.85).aspx">HDN_FILTERCHANGE</a>



<b>Reference</b>
 

 

