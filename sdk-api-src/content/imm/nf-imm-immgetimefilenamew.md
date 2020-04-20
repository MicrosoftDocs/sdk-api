---
UID: NF:imm.ImmGetIMEFileNameW
title: ImmGetIMEFileNameW function (imm.h)
description: Retrieves the file name of the IME associated with the specified input locale.helpviewer_keywords: ["ImmGetIMEFileName","ImmGetIMEFileName function [Internationalization for Windows Applications]","ImmGetIMEFileNameA","ImmGetIMEFileNameW","_win32_ImmGetIMEFileName","imm/ImmGetIMEFileName","imm/ImmGetIMEFileNameA","imm/ImmGetIMEFileNameW","intl.immgetimefilename"]
old-location: intl\immgetimefilename.htm
tech.root: Intl
ms.assetid: c2dafd0a-3cb9-4d9b-919b-c7ef86fb1cd4
ms.date: 12/05/2018
ms.keywords: ImmGetIMEFileName, ImmGetIMEFileName function [Internationalization for Windows Applications], ImmGetIMEFileNameA, ImmGetIMEFileNameW, _win32_ImmGetIMEFileName, imm/ImmGetIMEFileName, imm/ImmGetIMEFileNameA, imm/ImmGetIMEFileNameW, intl.immgetimefilename
f1_keywords:
- imm/ImmGetIMEFileName
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
req.unicode-ansi: ImmGetIMEFileNameW (Unicode) and ImmGetIMEFileNameA (ANSI)
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
- ImmGetIMEFileName
- ImmGetIMEFileNameA
- ImmGetIMEFileNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmGetIMEFileNameW function


## -description


Retrieves the file name of the IME associated with the specified input locale.


## -parameters




### -param HKL [in]

Input locale identifier.


### -param lpszFileName [out, optional]

Pointer to a buffer in which the function retrieves the file name. This parameter contains <b>NULL</b> when <i>uBufLen</i> is set to <b>NULL</b>.


### -param uBufLen [in]

Size, in bytes, of the output buffer. The application specifies 0 if the function is to return the buffer size needed to receive the file name, not including the terminating null character. For Unicode, <i>uBufLen</i> specifies the size in Unicode characters, not including the terminating null character.


## -returns



Returns the number of bytes in the file name copied to the output buffer. If the application sets <i>uBufLen</i> to 0, the function returns the size of the buffer required for the file name. In either case, the terminating null character is not included.

For Unicode, the function returns the number of Unicode characters copied into the output buffer, not including the Unicode terminating null character.




## -remarks



In the registry, the operating system stores the file name as the "IME name value" in the registry key HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Keyboard Layouts\HKL.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

