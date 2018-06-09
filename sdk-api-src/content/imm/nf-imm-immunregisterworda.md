---
UID: NF:imm.ImmUnregisterWordA
title: ImmUnregisterWordA function
author: windows-sdk-content
description: Removes a register string from the dictionary of the IME associated with the specified input locale.
old-location: intl\immunregisterword.htm
old-project: Intl
ms.assetid: 1724d516-bc9d-418f-9fe1-5c82eccc73c5
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: Any value from IME_REGWORD_STYLE_USER_FIRST to IME_REGWORD_STYLE_USER_LAST, IME_REGWORD_STYLE_EUDC, ImmUnregisterWord, ImmUnregisterWord function [Internationalization for Windows Applications], ImmUnregisterWordA, ImmUnregisterWordW, _win32_ImmUnregisterWord, imm/ImmUnregisterWord, imm/ImmUnregisterWordA, imm/ImmUnregisterWordW, intl.immunregisterword
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
req.unicode-ansi: ImmUnregisterWordW (Unicode) and ImmUnregisterWordA (ANSI)
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
 - Imm32.dll
api_name:
 - ImmUnregisterWord
 - ImmUnregisterWordA
 - ImmUnregisterWordW
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmUnregisterWordA function


## -description


Removes a register string from the dictionary of the IME associated with the specified input locale.


## -parameters




### -param HKL

TBD


### -param lpszReading [in]

Pointer to a null-terminated reading string associated with the string to remove.


### -param DWORD

TBD


### -param lpszUnregister [in]

Pointer to a null-terminated string specifying the register string to remove.


#### - dwStyle [in]

Style of the register string. This parameter can have any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IME_REGWORD_STYLE_EUDC"></a><a id="ime_regword_style_eudc"></a><dl>
<dt><b>IME_REGWORD_STYLE_EUDC</b></dt>
</dl>
</td>
<td width="60%">
The string is in the end-user-defined character (EUDC) range.

</td>
</tr>
<tr>
<td width="40%"><a id="Any_value_from_IME_REGWORD_STYLE_USER_FIRST_to_IME_REGWORD_STYLE_USER_LAST"></a><a id="any_value_from_ime_regword_style_user_first_to_ime_regword_style_user_last"></a><a id="ANY_VALUE_FROM_IME_REGWORD_STYLE_USER_FIRST_TO_IME_REGWORD_STYLE_USER_LAST"></a><dl>
<dt><b>Any value from IME_REGWORD_STYLE_USER_FIRST to IME_REGWORD_STYLE_USER_LAST</b></dt>
</dl>
</td>
<td width="60%">
The string is in a private style maintained by the specified IME.

</td>
</tr>
</table>
 


#### - hKL [in]

Input locale identifier.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

