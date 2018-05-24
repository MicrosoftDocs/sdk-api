---
UID: NF:userenv.ExpandEnvironmentStringsForUserW
title: ExpandEnvironmentStringsForUserW function
author: windows-driver-content
description: Expands the source string by using the environment block established for the specified user.
old-location: shell\ExpandEnvironmentStringsForUser.htm
old-project: shell
ms.assetid: d32fa6c8-035a-4c84-b210-5366f21b6c17
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ExpandEnvironmentStringsForUser, ExpandEnvironmentStringsForUser function [Windows Shell], ExpandEnvironmentStringsForUserA, ExpandEnvironmentStringsForUserW, _shell_ExpandEnvironmentStringsForUser, shell.ExpandEnvironmentStringsForUser, userenv/ExpandEnvironmentStringsForUser, userenv/ExpandEnvironmentStringsForUserA, userenv/ExpandEnvironmentStringsForUserW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExpandEnvironmentStringsForUserW (Unicode) and ExpandEnvironmentStringsForUserA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	ExpandEnvironmentStringsForUser
-	ExpandEnvironmentStringsForUserA
-	ExpandEnvironmentStringsForUserW
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# ExpandEnvironmentStringsForUserW function


## -description


Expands the source string by using the environment block established for the specified user.


## -parameters




### -param hToken [in, optional]

Type: <b>HANDLE</b>

Token for the user, returned from the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>, <a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>, <a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>, <a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>, or <a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a> function. The token must have TOKEN_IMPERSONATE and TOKEN_QUERY access. In addition, as of Windows 7 the token must also have TOKEN_DUPLICATE access. For more information, see <a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>.



If <i>hToken</i> is <b>NULL</b>, the environment block contains system variables only.


### -param lpSrc [in]

Type: <b>LPCTSTR</b>

Pointer to the null-terminated source string to be expanded.


### -param lpDest [out]

Type: <b>LPTSTR</b>

Pointer to a buffer that receives the expanded strings.


### -param dwSize [in]

Type: <b>DWORD</b>

Specifies the size of the <i>lpDest</i> buffer, in <b>TCHARs</b>.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The following is an example source string:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>%USERPROFILE%\ntuser.dat</pre>
</td>
</tr>
</table></span></div>
When <b>ExpandEnvironmentStringsForUser</b> returns, the destination string expands as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>C:\Documents and Settings\UserName\ntuser.dat</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/754c6aa9-b431-4d2b-a78b-c4da59ea8354">User Profiles Overview</a>



<a href="https://msdn.microsoft.com/86871866-bb90-4287-9640-0a6cd136a800">User Profiles Reference</a>
 

 

