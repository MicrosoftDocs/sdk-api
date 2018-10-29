---
UID: NF:imm.ImmDisableIME
title: ImmDisableIME function
author: windows-sdk-content
description: Disables the IME for a thread or for all threads in a process.
old-location: intl\immdisableime.htm
tech.root: Intl
ms.assetid: c563fc24-3c56-40ac-8539-8336d5231537
ms.author: windowssdkdev
ms.date: 10/26/2018
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
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - imm32.dll
 - ext-ms-win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmDisableIME
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmDisableIME function


## -description


Disables the IME for a thread or for all threads in a process.


## -parameters




### -param DWORD [in]

Identifier of the thread for which to disable the IME. The thread must be in the same process as the application calling this function. The application sets this parameter to 0 to disable the IME for the current thread. The application specifies -1 to disable the IME for all threads in the current process.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



The application must call this function before the first top-level window in the thread receives the <a href="https://msdn.microsoft.com/en-us/library/ms632619(v=VS.85).aspx">WM_CREATE</a> message. Thus, the application must call this function in one of the following places:

<ul>
<li>Any time before calling <a href="https://msdn.microsoft.com/en-us/library/ms632679(v=VS.85).aspx">CreateWindow</a> to create the first top-level window</li>
<li>In the <a href="https://msdn.microsoft.com/en-us/library/ms632635(v=VS.85).aspx">WM_NCCREATE</a> handler for first top-level window</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

