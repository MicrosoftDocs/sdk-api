---
UID: NF:imm.ImmDisableIME
title: ImmDisableIME function (imm.h)
description: Disables the IME for a thread or for all threads in a process.
helpviewer_keywords: ["ImmDisableIME","ImmDisableIME function [Internationalization for Windows Applications]","_win32_ImmDisableIME","imm/ImmDisableIME","intl.immdisableime"]
old-location: intl\immdisableime.htm
tech.root: Intl
ms.assetid: c563fc24-3c56-40ac-8539-8336d5231537
ms.date: 12/05/2018
ms.keywords: ImmDisableIME, ImmDisableIME function [Internationalization for Windows Applications], _win32_ImmDisableIME, imm/ImmDisableIME, intl.immdisableime
f1_keywords:
- imm/ImmDisableIME
dev_langs:
- c++
req.header: imm.h
req.include-header: Immdev.h, Windows.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



The application must call this function before the first top-level window in the thread receives the <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-create">WM_CREATE</a> message. Thus, the application must call this function in one of the following places:

<ul>
<li>Any time before calling <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> to create the first top-level window</li>
<li>In the <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-nccreate">WM_NCCREATE</a> handler for first top-level window</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

