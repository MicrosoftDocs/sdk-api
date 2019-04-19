---
UID: NF:commctrl.Header_SetOrderArray
title: Header_SetOrderArray macro (commctrl.h)
author: windows-sdk-content
description: Sets the left-to-right order of header items. You can use this macro or send the HDM_SETORDERARRAY message explicitly.
old-location: controls\Header_SetOrderArray.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setorderarray.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Header_SetOrderArray, Header_SetOrderArray macro [Windows Controls], _win32_Header_SetOrderArray, _win32_Header_SetOrderArray_cpp, commctrl/Header_SetOrderArray, controls.Header_SetOrderArray, controls._win32_Header_SetOrderArray
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
 - Header_SetOrderArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Header_SetOrderArray macro


## -description


Sets the left-to-right order of header items. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775369(v=VS.85).aspx">HDM_SETORDERARRAY</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


### -param iCount

Type: <b>int</b>

The size of the buffer at 
					<i>lpiArray</i>, in elements. This value must equal the value returned by <a href="https://msdn.microsoft.com/en-us/library/Bb775337(v=VS.85).aspx">HDM_GETITEMCOUNT</a>. 


### -param lpi

Type: <b>int*</b>

A pointer to an array that specifies the order in which items should be displayed, from left to right. For example, if the contents of the array are {2,0,1}, the control displays item 2, item 0, and item 1, from left to right. 

