---
UID: NF:imm.ImmGetDescriptionA
title: ImmGetDescriptionA function (imm.h)
author: windows-sdk-content
description: Copies the description of the IME to the specified buffer.
old-location: intl\immgetdescription.htm
tech.root: Intl
ms.assetid: 62f4efc8-7b46-4d8e-a6a2-2f346efe8ba6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImmGetDescription, ImmGetDescription function [Internationalization for Windows Applications], ImmGetDescriptionA, ImmGetDescriptionW, _win32_ImmGetDescription, imm/ImmGetDescription, imm/ImmGetDescriptionA, imm/ImmGetDescriptionW, intl.immgetdescription
ms.topic: function
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed., East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmGetDescriptionW (Unicode) and ImmGetDescriptionA (ANSI)
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
 - ImmGetDescription
 - ImmGetDescriptionA
 - ImmGetDescriptionW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmGetDescriptionA function


## -description


Copies the description of the IME to the specified buffer.


## -parameters




### -param HKL [in]

Input locale identifier.


### -param lpszDescription [out, optional]

Pointer to a buffer in which the function retrieves the null-terminated string describing the IME.


### -param uBufLen [in]

Size, in characters, of the output buffer. The application sets this parameter to 0 if the function is to return the buffer size needed for the complete description, excluding the terminating null character.

<b>Windows NT, Windows 2000, Windows XP:</b> The size of the buffer is in Unicode characters, each consisting of two bytes. If the parameter is set to 0, the function returns the size of the buffer required in Unicode characters, excluding the Unicode terminating null character.


## -returns



Returns the number of characters copied to the output buffer. If the application sets the <i>uBufLen</i> parameter to 0, the function returns the size of the buffer required to receive the description. Neither value includes the terminating null character. For Unicode, the function returns the number of Unicode characters, not including the Unicode terminating null character.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

