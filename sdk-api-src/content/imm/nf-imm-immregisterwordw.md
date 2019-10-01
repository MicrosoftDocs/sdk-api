---
UID: NF:imm.ImmRegisterWordW
title: ImmRegisterWordW function (imm.h)
author: windows-sdk-content
description: Registers a string with the dictionary of the IME associated with the specified input locale.
old-location: intl\immregisterword.htm
tech.root: Intl
ms.assetid: c5a507f3-5908-4f44-be7a-7feba8bfe378
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Any value in the range from IME_REGWORD_STYLE_USER_FIRST to IME_REGWORD_STYLE_USER_LAST, IME_REGWORD_STYLE_EUDC, ImmRegisterWord, ImmRegisterWord function [Internationalization for Windows Applications], ImmRegisterWordA, ImmRegisterWordW, _win32_ImmRegisterWord, imm/ImmRegisterWord, imm/ImmRegisterWordA, imm/ImmRegisterWordW, intl.immregisterword
ms.topic: function
f1_keywords: 
 - "imm/ImmRegisterWord"
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmRegisterWordW (Unicode) and ImmRegisterWordA (ANSI)
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
 - ImmRegisterWord
 - ImmRegisterWordA
 - ImmRegisterWordW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmRegisterWordW function


## -description


Registers a string with the dictionary of the IME associated with the specified input locale.


## -parameters




### -param HKL [in]

Input locale identifier.


### -param lpszReading [in]

Pointer to a null-terminated reading string associated with the string to register.


### -param DWORD [in]

Style of the string to register. This parameter can have any of the following values.

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
The string is in the end-user-defined (EUDC) range.

</td>
</tr>
<tr>
<td width="40%"><a id="Any_value_in_the_range_from_IME_REGWORD_STYLE_USER_FIRST_to_IME_REGWORD_STYLE_USER_LAST"></a><a id="any_value_in_the_range_from_ime_regword_style_user_first_to_ime_regword_style_user_last"></a><a id="ANY_VALUE_IN_THE_RANGE_FROM_IME_REGWORD_STYLE_USER_FIRST_TO_IME_REGWORD_STYLE_USER_LAST"></a><dl>
<dt><b>Any value in the range from IME_REGWORD_STYLE_USER_FIRST to IME_REGWORD_STYLE_USER_LAST</b></dt>
</dl>
</td>
<td width="60%">
The string has a private style maintained by the specified IME. See the Remarks section for more details.

</td>
</tr>
</table>
 


### -param lpszRegister [in]

Pointer to the null-terminated string to register.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



An IME independent software vendor (ISV) can define private styles for an IME in the IME_REGWORD_STYLE_USER_FIRST and IME_REGWORD_STYLE_USER_LAST values. For example:


```cpp
#define MSIME_NOUN (IME_REGWORD_STYLE_USER_FIRST)
#define MSIME_VERB (IME_REGWORD_STYLE_USER_FIRST + 1)

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

