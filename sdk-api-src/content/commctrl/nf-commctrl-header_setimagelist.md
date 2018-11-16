---
UID: NF:commctrl.Header_SetImageList
title: Header_SetImageList macro
author: windows-sdk-content
description: Assigns an image list to an existing header control. You can use this macro or send the HDM_SETIMAGELIST message explicitly.
old-location: controls\Header_SetImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setimagelist.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Header_SetImageList, Header_SetImageList macro [Windows Controls], _win32_Header_SetImageList, _win32_Header_SetImageList_cpp, commctrl/Header_SetImageList, controls.Header_SetImageList, controls._win32_Header_SetImageList
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
 - Header_SetImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- Header_SetImageList
: 
---

# Header_SetImageList macro


## -description


Assigns an image list to an existing header control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775365(v=VS.85).aspx">HDM_SETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to a header control. 


### -param himl

Type: <b>HIMAGELIST</b>

A handle to an image list. 

