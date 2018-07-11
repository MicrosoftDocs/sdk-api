---
UID: NF:commctrl.Header_GetItemCount
title: Header_GetItemCount macro
author: windows-sdk-content
description: Gets a count of the items in a header control. You can use this macro or send the HDM_GETITEMCOUNT message explicitly.
old-location: controls\Header_GetItemCount.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getitemcount.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: Header_GetItemCount, Header_GetItemCount macro [Windows Controls], _win32_Header_GetItemCount, _win32_Header_GetItemCount_cpp, commctrl/Header_GetItemCount, controls.Header_GetItemCount, controls._win32_Header_GetItemCount
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
 - Header_GetItemCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Header_GetItemCount macro


## -description


Gets a count of the items in a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb775337(v=VS.85).aspx">HDM_GETITEMCOUNT</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


## -remarks



The <b>Header_GetItemCount</b> macro is defined as follows. 

<pre class="syntax" xml:space="preserve"><code>#define Header_GetItemCount(hwndHD)   \

       (int)SendMessage((hwndHD), HDM_GETITEMCOUNT, 0, 0L)</code></pre>


