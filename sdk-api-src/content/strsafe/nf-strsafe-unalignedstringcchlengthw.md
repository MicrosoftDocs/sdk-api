---
UID: NF:strsafe.UnalignedStringCchLengthW
title: UnalignedStringCchLengthW function
author: windows-driver-content
description: Determines whether a string exceeds the specified length, in characters.
old-location: menurc\unalignedstringcchlength.htm
old-project: menurc
ms.assetid: 35571305-9ef4-4215-ad88-80590e9b89cc
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: StringCchLengthA, UnalignedStringCchLength, UnalignedStringCchLength function [Menus and Other Resources], UnalignedStringCchLengthW, menurc.unalignedstringcchlength, strsafe/StringCchLengthA, strsafe/UnalignedStringCchLength, strsafe/UnalignedStringCchLengthW
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
req.unicode-ansi: UnalignedStringCchLengthW (Unicode) and StringCchLengthA (ANSI)
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
-	UnalignedStringCchLength
-	StringCchLengthA
-	UnalignedStringCchLengthW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UnalignedStringCchLengthW function


## -description


Determines whether a string exceeds the specified length, in characters.

The function is similar to <a href="https://msdn.microsoft.com/4b29469a-e9a8-4309-9d19-db74a8bd6038">StringCchLength</a>, but it accepts an unaligned string pointer.


## -parameters




### -param psz [in]

The string whose length is to be checked.


### -param cchMax [in]

The maximum number of characters allowed in <i>psz</i>, including the terminating null character. This value cannot exceed <b>STRSAFE_MAX_CCH</b>.


### -param pcchLength [out, optional]

The number of characters in <i>psz</i>, not including the terminating null character. This value is valid only if <i>pcch</i> is not <b>NULL</b> and the function succeeds.


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
The string at <i>psz</i> was not <b>NULL</b>, and the length of the string (including the terminating null character) is less than or equal to <i>cchMax</i> characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>psz</i> is <b>NULL</b>, <i>cchMax</i> is larger than <b>STRSAFE_MAX_CCH</b>, or <i>psz</i> is longer than <i>cchMax</i>.

</td>
</tr>
</table>
 



