---
UID: NF:immdev.ImmEnumRegisterWordA
title: ImmEnumRegisterWordA function (immdev.h)

description: Enumerates the register strings having the specified reading string, style, and register string.
old-location: intl\immenumregisterword.htm
tech.root: Intl
ms.assetid: ebeed3f9-1164-49d8-a7af-61244976643b

ms.date: 12/05/2018
ms.keywords: ImmEnumRegisterWord, ImmEnumRegisterWord function [Internationalization for Windows Applications], ImmEnumRegisterWordA, ImmEnumRegisterWordW, _win32_ImmEnumRegisterWord, imm/ImmEnumRegisterWord, imm/ImmEnumRegisterWordA, imm/ImmEnumRegisterWordW, intl.immenumregisterword
ms.topic: function
f1_keywords: 
 - "immdev/ImmEnumRegisterWord"
dev_langs:
 - c++
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
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
api_name:
 - ImmEnumRegisterWord
 - ImmEnumRegisterWordA
 - ImmEnumRegisterWordW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmEnumRegisterWordA function


## -description


Enumerates the register strings having the specified reading string, style, and register string.


## -parameters




### -param HKL [in]

Input locale identifier.


#### - REGISTERWORDENUMPROCA [in]

Pointer to the callback function. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/imm/nc-imm-registerwordenumproca">EnumRegisterWordProc</a>.


### -param lpszReading [in, optional]

Pointer to the reading string to enumerate. The application sets this parameter to <b>NULL</b> if the function is to enumerate all available reading strings that match the <i>dwStyle</i> and <i>lpszRegister</i> settings.


### -param DWORD [in]

Style to enumerate. The application specifies 0 if the function is to enumerate all available styles that match the <i>lpszReading</i> and <i>lpszRegister</i> settings.


### -param lpszRegister [in, optional]

Pointer to the register string to enumerate. The application sets this parameter to <b>NULL</b> if the function is to enumerate all register strings that match the <i>lpszReading</i> and <i>dwStyle</i> settings.


### -param LPVOID [in]

Pointer to application-supplied data. The function passes this data to the callback function.


## -returns



Returns the last value returned by the callback function, with the meaning defined by the application. The function returns 0 if it cannot enumerate the register strings.




## -remarks



If <i>dwStyle</i> is set to 0 and both <i>lpszReading</i> and <i>lpszRegister</i> are set to <b>NULL</b>, this function enumerates all register strings in the IME dictionary.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imm/nc-imm-registerwordenumproca">EnumRegisterWordProc</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

