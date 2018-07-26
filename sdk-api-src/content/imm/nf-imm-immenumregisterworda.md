---
UID: NF:imm.ImmEnumRegisterWordA
title: ImmEnumRegisterWordA function
author: windows-sdk-content
description: Enumerates the register strings having the specified reading string, style, and register string.
old-location: intl\immenumregisterword.htm
old-project: Intl
ms.assetid: ebeed3f9-1164-49d8-a7af-61244976643b
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: ImmEnumRegisterWord, ImmEnumRegisterWord function [Internationalization for Windows Applications], ImmEnumRegisterWordA, ImmEnumRegisterWordW, _win32_ImmEnumRegisterWord, imm/ImmEnumRegisterWord, imm/ImmEnumRegisterWordA, imm/ImmEnumRegisterWordW, intl.immenumregisterword
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmEnumRegisterWordW (Unicode) and ImmEnumRegisterWordA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMECOMPOSITIONSTRINGINFO, *LPIMECOMPOSITIONSTRINGINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - imm32.dll
api_name:
 - ImmEnumRegisterWord
 - ImmEnumRegisterWordA
 - ImmEnumRegisterWordW
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmEnumRegisterWordA function


## -description


Enumerates the register strings having the specified reading string, style, and register string.


## -parameters




### -param HKL

TBD


### -param REGISTERWORDENUMPROCA

TBD


### -param lpszReading [in, optional]

Pointer to the reading string to enumerate. The application sets this parameter to <b>NULL</b> if the function is to enumerate all available reading strings that match the <i>dwStyle</i> and <i>lpszRegister</i> settings.


### -param DWORD

TBD


### -param lpszRegister [in, optional]

Pointer to the register string to enumerate. The application sets this parameter to <b>NULL</b> if the function is to enumerate all register strings that match the <i>lpszReading</i> and <i>dwStyle</i> settings.


### -param LPVOID

TBD




#### - dwStyle [in]

Style to enumerate. The application specifies 0 if the function is to enumerate all available styles that match the <i>lpszReading</i> and <i>lpszRegister</i> settings.


#### - hKL [in]

Input locale identifier.


#### - lpData [in]

Pointer to application-supplied data. The function passes this data to the callback function.


#### - lpfnEnumProc [in]

Pointer to the callback function. For more information, see <a href="https://msdn.microsoft.com/06038c87-3553-47de-ba9f-b9c65ea9920b">EnumRegisterWordProc</a>.


## -returns



Returns the last value returned by the callback function, with the meaning defined by the application. The function returns 0 if it cannot enumerate the register strings.




## -remarks



If <i>dwStyle</i> is set to 0 and both <i>lpszReading</i> and <i>lpszRegister</i> are set to <b>NULL</b>, this function enumerates all register strings in the IME dictionary.




## -see-also




<a href="https://msdn.microsoft.com/06038c87-3553-47de-ba9f-b9c65ea9920b">EnumRegisterWordProc</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

