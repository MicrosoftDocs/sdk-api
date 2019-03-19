---
UID: NF:commctrl.Header_OrderToIndex
title: Header_OrderToIndex macro (commctrl.h)
author: windows-sdk-content
description: Retrieves an index value for an item based on its order in the header control. You can use this macro or send the HDM_ORDERTOINDEX message explicitly.
old-location: controls\Header_OrderToIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_ordertoindex.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Header_OrderToIndex, Header_OrderToIndex macro [Windows Controls], _win32_Header_OrderToIndex, _win32_Header_OrderToIndex_cpp, commctrl/Header_OrderToIndex, controls.Header_OrderToIndex, controls._win32_Header_OrderToIndex
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
 - Header_OrderToIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Header_OrderToIndex macro


## -description


Retrieves an index value for an item based on its order in the header control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775355(v=VS.85).aspx">HDM_ORDERTOINDEX</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


### -param i

Type: <b>int</b>

The order that the item appears within the header control, from left to right. The index value of the item in the far left column would be 0, the next item to the right would be 1, and so on. 

