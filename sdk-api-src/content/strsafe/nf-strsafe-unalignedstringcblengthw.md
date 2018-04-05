---
UID: NF:strsafe.UnalignedStringCbLengthW
title: UnalignedStringCbLengthW function
author: windows-driver-content
description: Determines whether a string exceeds the specified length, in bytes.
old-location: menurc\unalignedstringcblength.htm
old-project: menurc
ms.assetid: 2aa104f8-44e2-4896-86d8-5e2b6d9d7b73
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: StringCbLengthA, UnalignedStringCbLength, UnalignedStringCbLength function [Menus and Other Resources], UnalignedStringCbLengthW, menurc.unalignedstringcblength, strsafe/StringCbLengthA, strsafe/UnalignedStringCbLength, strsafe/UnalignedStringCbLengthW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UnalignedStringCbLengthW (Unicode) and StringCbLengthA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AM_DVD_RENDERSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	StrSafe.h
api_name:
-	UnalignedStringCbLength
-	StringCbLengthA
-	UnalignedStringCbLengthW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UnalignedStringCbLengthW function


## -description


Determines whether a string exceeds the specified length, in bytes.

The function is similar to <a href="https://msdn.microsoft.com/a1aa834c-53e7-4321-9db4-86f32ef31dc4">StringCbLength</a>, but it accepts an unaligned string pointer.


## -parameters




### -param psz [in]

The string whose length is to be checked.


### -param cbMax [in]

The maximum number of bytes allowed in <i>psz</i>, including those used for the terminating null character. This value cannot exceed <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.


### -param pcbLength [out, optional]

The number of bytes in <i>psz</i>, excluding those used for the terminating null character. This value is valid only if <i>pcb</i> is not <b>NULL</b> and the function succeeds.




## -returns



This function can return one of the following values. It is strongly recommended that you use the <a href="https://msdn.microsoft.com/7a258b0b-d214-46c5-be0a-6493cd14a0e5">SUCCEEDED</a> and <a href="https://msdn.microsoft.com/d9c4ff73-c255-4a82-b901-23bd5b41ee6c">FAILED</a> macros to test the return value of this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The string at <i>psz</i> was not <b>NULL</b>, and the length of the string (including the terminating null character) is less than or equal to <i>cbMax</i> characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>psz</i> is <b>NULL</b>, <i>cbMax</i> is larger than <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>, or <i>psz</i> is longer than <i>cbMax</i>.

</td>
</tr>
</table>
 



