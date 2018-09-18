---
UID: NF:shlobj_core.DAD_AutoScroll
title: DAD_AutoScroll function
author: windows-sdk-content
description: Scrolls the window while an image is being dragged.
old-location: shell\DAD_AutoScroll.htm
tech.root: shell
ms.assetid: 3c5af682-8497-477e-8222-3eb37d1e295f
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: DAD_AutoScroll, DAD_AutoScroll function [Windows Shell], shell.DAD_AutoScroll, shell_DAD_AutoScroll, shlobj_core/DAD_AutoScroll
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - DAD_AutoScroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DAD_AutoScroll function


## -description


<p class="CCE_Message">[<b>DAD_AutoScroll</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions.]

Scrolls the window while an image is being dragged.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window being scrolled.


### -param pad [in]

Type: <b><a href="https://msdn.microsoft.com/4229dd3b-1fc7-4cc7-bcc9-4e25bdc17c11">AUTO_SCROLL_DATA</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/4229dd3b-1fc7-4cc7-bcc9-4e25bdc17c11">AUTO_SCROLL_DATA</a> structure.


### -param pptNow [in]

Type: <b>const <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to the current scroll coordinates.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.




## -remarks



The function is successful and the window scrolls only when the <b>bFull</b> parameter of the <a href="https://msdn.microsoft.com/4229dd3b-1fc7-4cc7-bcc9-4e25bdc17c11">AUTO_SCROLL_DATA</a> structure is <b>TRUE</b>. Each time this function is called, as long as <b>bFull</b> is <b>FALSE</b>, the <b>iNextSample</b> parameter is incremented by 1 and the current scroll coordinates and time are returned in the <b>AUTO_SCROLL_DATA</b> structure. When <b>iNextSample</b> is equal to NUM_POINTS, <b>bFull</b> is set to <b>TRUE</b>, the function succeeds, and the window scrolls.





## -see-also




<a href="https://msdn.microsoft.com/4229dd3b-1fc7-4cc7-bcc9-4e25bdc17c11">AUTO_SCROLL_DATA</a>
 

 

