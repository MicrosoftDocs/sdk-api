---
UID: NF:imm.ImmDisableIME
title: ImmDisableIME function
author: windows-driver-content
description: Disables the IME for a thread or for all threads in a process.
old-location: intl\immdisableime.htm
old-project: Intl
ms.assetid: c563fc24-3c56-40ac-8539-8336d5231537
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ImmDisableIME, ImmDisableIME function [Internationalization for Windows Applications], _win32_ImmDisableIME, imm/ImmDisableIME, intl.immdisableime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
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
req.typenames: IMECOMPOSITIONSTRINGINFO, *LPIMECOMPOSITIONSTRINGINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	imm32.dll
-	ext-ms-win-imm-l1-1-0.dll
-	ext-ms-win-imm-l1-1-1.dll
api_name:
-	ImmDisableIME
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmDisableIME function


## -description


Disables the IME for a thread or for all threads in a process.


## -parameters




### -param DWORD

TBD




#### - idThread [in]

Identifier of the thread for which to disable the IME. The thread must be in the same process as the application calling this function. The application sets this parameter to 0 to disable the IME for the current thread. The application specifies -1 to disable the IME for all threads in the current process.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



The application must call this function before the first top-level window in the thread receives the <a href="_win32_wm_create_cpp">WM_CREATE</a> message. Thus, the application must call this function in one of the following places:

<ul>
<li>Any time before calling <a href="_win32_createwindow_cpp">CreateWindow</a> to create the first top-level window</li>
<li>In the <a href="_win32_wm_nccreate_cpp">WM_NCCREATE</a> handler for first top-level window</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

