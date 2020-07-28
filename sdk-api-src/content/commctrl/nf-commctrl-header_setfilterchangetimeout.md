---
UID: NF:commctrl.Header_SetFilterChangeTimeout
title: Header_SetFilterChangeTimeout macro (commctrl.h)
description: Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an HDN_FILTERCHANGE notification. You can use this macro or send the HDM_SETFILTERCHANGETIMEOUT message explicitly.
helpviewer_keywords: ["Header_SetFilterChangeTimeout","Header_SetFilterChangeTimeout macro [Windows Controls]","_win32_Header_SetFilterChangeTimeout","_win32_Header_SetFilterChangeTimeout_cpp","commctrl/Header_SetFilterChangeTimeout","controls.Header_SetFilterChangeTimeout","controls._win32_Header_SetFilterChangeTimeout"]
old-location: controls\Header_SetFilterChangeTimeout.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setfilterchangetimeout.htm
ms.date: 12/05/2018
ms.keywords: Header_SetFilterChangeTimeout, Header_SetFilterChangeTimeout macro [Windows Controls], _win32_Header_SetFilterChangeTimeout, _win32_Header_SetFilterChangeTimeout_cpp, commctrl/Header_SetFilterChangeTimeout, controls.Header_SetFilterChangeTimeout, controls._win32_Header_SetFilterChangeTimeout
f1_keywords:
- commctrl/Header_SetFilterChangeTimeout
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
- Header_SetFilterChangeTimeout
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Header_SetFilterChangeTimeout macro


## -description


Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an <a href="https://docs.microsoft.com/windows/desktop/Controls/hdn-filterchange">HDN_FILTERCHANGE</a> notification. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/hdm-setfilterchangetimeout">HDM_SETFILTERCHANGETIMEOUT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control. 


### -param i

Type: <b>int</b>

The timeout value, in milliseconds. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/hdm-setfilterchangetimeout">HDM_SETFILTERCHANGETIMEOUT</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/hdn-filterchange">HDN_FILTERCHANGE</a>



<b>Reference</b>
 

 

