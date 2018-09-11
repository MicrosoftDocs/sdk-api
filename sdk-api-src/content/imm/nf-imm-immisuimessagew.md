---
UID: NF:imm.ImmIsUIMessageW
title: ImmIsUIMessageW function
author: windows-sdk-content
description: Checks for messages intended for the IME window and sends those messages to the window.
old-location: intl\immisuimessage.htm
tech.root: Intl
ms.assetid: 9c07c7b8-87cb-4bcb-a837-20f582ff7712
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: ImmIsUIMessage, ImmIsUIMessage function [Internationalization for Windows Applications], ImmIsUIMessageA, ImmIsUIMessageW, _win32_ImmIsUIMessage, imm/ImmIsUIMessage, imm/ImmIsUIMessageA, imm/ImmIsUIMessageW, intl.immisuimessage
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
---

# ImmIsUIMessageW function


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

<b>Windows Me/98:</b> This function has only an ANSI version. To receive Unicode characters from a Unicode-based IME, the application should use <a href="https://msdn.microsoft.com/6309e5b4-36ce-4899-be33-d7bf0d828d3d">ImmGetCompositionString</a>.




## -see-also




<a href="https://msdn.microsoft.com/6309e5b4-36ce-4899-be33-d7bf0d828d3d">ImmGetCompositionString</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

