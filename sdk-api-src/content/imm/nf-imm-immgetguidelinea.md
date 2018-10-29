---
UID: NF:imm.ImmGetGuideLineA
title: ImmGetGuideLineA function
author: windows-sdk-content
description: Retrieves information about errors. Applications use the information for user notifications.
old-location: intl\immgetguideline.htm
tech.root: Intl
ms.assetid: f6639061-0ad9-4f42-b5d4-66ad3f6298aa
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GGL_INDEX, GGL_LEVEL, GGL_PRIVATE, GGL_STRING, ImmGetGuideLine, ImmGetGuideLine function [Internationalization for Windows Applications], ImmGetGuideLineA, ImmGetGuideLineW, _win32_ImmGetGuideLine, imm/ImmGetGuideLine, imm/ImmGetGuideLineA, imm/ImmGetGuideLineW, intl.immgetguideline
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
req.unicode-ansi: ImmGetGuideLineW (Unicode) and ImmGetGuideLineA (ANSI)
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
 - ImmGetGuideLine
 - ImmGetGuideLineA
 - ImmGetGuideLineW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmGetGuideLineA function


## -description


Retrieves information about errors. Applications use the information for user notifications.


## -parameters




### -param arg1 [in]

Handle to the input context.


### -param dwIndex [in]

Type of guideline information to retrieve. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GGL_LEVEL"></a><a id="ggl_level"></a><dl>
<dt><b>GGL_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
Return the error level.

</td>
</tr>
<tr>
<td width="40%"><a id="GGL_INDEX"></a><a id="ggl_index"></a><dl>
<dt><b>GGL_INDEX</b></dt>
</dl>
</td>
<td width="60%">
Return the error index.

</td>
</tr>
<tr>
<td width="40%"><a id="GGL_STRING"></a><a id="ggl_string"></a><dl>
<dt><b>GGL_STRING</b></dt>
</dl>
</td>
<td width="60%">
Return the error message string.

</td>
</tr>
<tr>
<td width="40%"><a id="GGL_PRIVATE"></a><a id="ggl_private"></a><dl>
<dt><b>GGL_PRIVATE</b></dt>
</dl>
</td>
<td width="60%">
Return information about reverse conversion.

</td>
</tr>
</table>
 


### -param lpBuf [out, optional]

Pointer to a buffer in which the function retrieves the error message string. This parameter contains <b>NULL</b> if <i>dwIndex</i> is not GGL_STRING or GGL_PRIVATE or if <i>dwBufLen</i> is set to 0.


### -param dwBufLen [in]

Size, in bytes, of the output buffer. The application sets this parameter to 0 if the function is to return the buffer size needed to receive the error message string, not including the terminating null character.


## -returns



Returns an error level, an error index, or the size of an error message string, depending on the value of the <i>dwIndex</i> parameter. If <i>dwIndex</i> is GGL_LEVEL, the return is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>GL_LEVEL_ERROR</td>
<td>Error. The IME might not be able to continue.</td>
</tr>
<tr>
<td>GL_LEVEL_FATAL</td>
<td>Fatal error. The IME cannot continue, and data might be lost.</td>
</tr>
<tr>
<td>GL_LEVEL_INFORMATION</td>
<td>No error. Information is available for the user.</td>
</tr>
<tr>
<td>GL_LEVEL_NOGUIDELINE</td>
<td>No error. Remove previous error message if still visible.</td>
</tr>
<tr>
<td>GL_LEVEL_WARNING</td>
<td>Unexpected input or other result. The user should be warned, but the IME can continue.</td>
</tr>
</table>
 

If <i>dwIndex</i> is GGL_INDEX, the return value is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>GL_ID_CANNOTSAVE</td>
<td>The dictionary or the statistics data cannot be saved.</td>
</tr>
<tr>
<td>GL_ID_NOCONVERT</td>
<td>The IME cannot convert any more.</td>
</tr>
<tr>
<td>GL_ID_NODICTIONARY</td>
<td>The IME cannot find the dictionary, or the dictionary has an unexpected format.</td>
</tr>
<tr>
<td>GL_ID_NOMODULE</td>
<td>The IME cannot find the module that is needed.</td>
</tr>
<tr>
<td>GL_ID_READINGCONFLICT</td>
<td>A reading conflict occurred. For example, some vowels cannot be put together to form one character.</td>
</tr>
<tr>
<td>GL_ID_TOOMANYSTROKE</td>
<td>There are too many strokes for one character or one clause.</td>
</tr>
<tr>
<td>GL_ID_TYPINGERROR</td>
<td>Typing error. The IME cannot handle this typing.</td>
</tr>
<tr>
<td>GL_ID_UNKNOWN</td>
<td>Unknown error. Refer to the error message string.</td>
</tr>
<tr>
<td>GL_ID_INPUTREADING</td>
<td>The IME is accepting reading character input from the end user.</td>
</tr>
<tr>
<td>GL_ID_INPUTRADICAL</td>
<td>The IME is accepting radical character input from the end user.</td>
</tr>
<tr>
<td>GL_ID_INPUTCODE</td>
<td>The IME is accepting character code input from the end user.</td>
</tr>
<tr>
<td>GL_ID_CHOOSECANDIDATE</td>
<td>The IME is accepting candidate string selection from the end user.</td>
</tr>
<tr>
<td>GL_ID_REVERSECONVERSION</td>
<td>Information about reverse conversion is available by calling <b>ImmGetGuideLine</b>, specifying GGL_PRIVATE. The information retrieved is in <a href="https://msdn.microsoft.com/d60b28fb-0cdd-43b4-8d99-cb829bea6679">CANDIDATELIST</a> format.</td>
</tr>
</table>
 

If <i>dwIndex</i> is GGL_STRING, the return value is the number of bytes of the string copied to the buffer. However, if <i>dwBufLen</i> is 0, the return value is the buffer size needed to receive the string, not including the terminating null character. For Unicode, if <i>dwBufLen</i> is 0, the return value is the size, in bytes not including the Unicode terminating null character.

If <i>dwIndex</i> is GGL_PRIVATE, the return value is the number of bytes of information copied to the buffer. If <i>dwIndex</i> is GGL_PRIVATE and <i>dwBufLen</i> is 0, the return value is the buffer size needed to receive the information.




## -remarks



Applications typically call this function after receiving an <a href="https://msdn.microsoft.com/b898283a-af1a-484f-bfb8-e5d5c0ac8ee1">IMN_GUIDELINE</a> command.




## -see-also




<a href="https://msdn.microsoft.com/d60b28fb-0cdd-43b4-8d99-cb829bea6679">CANDIDATELIST</a>



<a href="https://msdn.microsoft.com/b898283a-af1a-484f-bfb8-e5d5c0ac8ee1">IMN_GUIDELINE</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

