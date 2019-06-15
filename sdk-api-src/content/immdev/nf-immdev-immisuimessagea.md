---
UID: NF:immdev.ImmIsUIMessageA
title: ImmIsUIMessageA function (immdev.h)
author: windows-sdk-content
description: Checks for messages intended for the IME window and sends those messages to the window.
old-location: intl\immisuimessage.htm
tech.root: Intl
ms.assetid: 9c07c7b8-87cb-4bcb-a837-20f582ff7712
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImmIsUIMessage, ImmIsUIMessage function [Internationalization for Windows Applications], ImmIsUIMessageA, ImmIsUIMessageW, _win32_ImmIsUIMessage, imm/ImmIsUIMessage, imm/ImmIsUIMessageA, imm/ImmIsUIMessageW, intl.immisuimessage
ms.topic: function
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmIsUIMessageW (Unicode) and ImmIsUIMessageA (ANSI)
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
 - Imm32.dll
api_name:
 - ImmIsUIMessage
 - ImmIsUIMessageA
 - ImmIsUIMessageW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmIsUIMessageA function


## -description


Checks for messages intended for the IME window and sends those messages to the window.


## -parameters




### -param HWND [in]

Handle to a window belonging to the IME window class.


### -param UINT [in]

Message to check.


### -param WPARAM [in]

Message-specific parameter.


### -param LPARAM [in]

Message-specific parameter.


## -returns



Returns a nonzero value if the message is processed by the IME window, or 0 otherwise.




## -remarks



An application typically uses this function to display a composition string or candidate list specified by the IME. If <i>hWndIME</i> is <b>NULL</b>, the function determines if the message is a user interface message.

<b>Windows Me/98:</b> This function has only an ANSI version. To receive Unicode characters from a Unicode-based IME, the application should use <a href="https://docs.microsoft.com/windows/desktop/api/imm/nf-imm-immgetcompositionstringa">ImmGetCompositionString</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imm/nf-imm-immgetcompositionstringa">ImmGetCompositionString</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

