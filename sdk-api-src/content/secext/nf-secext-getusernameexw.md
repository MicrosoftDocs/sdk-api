---
UID: NF:secext.GetUserNameExW
title: GetUserNameExW function (secext.h)
description: Retrieves the name of the user or other security principal associated with the calling thread. You can specify the format of the returned name.helpviewer_keywords: ["GetUserNameEx","GetUserNameEx function","GetUserNameExA","GetUserNameExW","_win32_getusernameex","base.getusernameex","secext/GetUserNameEx","secext/GetUserNameExA","secext/GetUserNameExW"]
old-location: base\getusernameex.htm
tech.root: SysInfo
ms.assetid: 7e7d618b-2e64-4b0b-aed3-f3221b0443ca
ms.date: 12/05/2018
ms.keywords: GetUserNameEx, GetUserNameEx function, GetUserNameExA, GetUserNameExW, _win32_getusernameex, base.getusernameex, secext/GetUserNameEx, secext/GetUserNameExA, secext/GetUserNameExW
f1_keywords:
- secext/GetUserNameEx
dev_langs:
- c++
req.header: secext.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetUserNameExW (Unicode) and GetUserNameExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Secur32.dll
api_name:
- GetUserNameEx
- GetUserNameExA
- GetUserNameExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetUserNameExW function


## -description


Retrieves the name of the user or other security principal associated with the calling thread. You can specify the format of the returned name.

If the thread is impersonating a client, 
<b>GetUserNameEx</b> returns the name of the client.


## -parameters




### -param NameFormat [in]

The format of the name. This parameter is a value from the 
<a href="https://docs.microsoft.com/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a> enumeration type. It cannot be <b>NameUnknown</b>. If the user account is not in a domain, only <b>NameSamCompatible</b> is supported.


### -param lpNameBuffer [out]

A pointer to a buffer that receives the name in the specified format. The buffer must include space for the terminating null character.


### -param nSize [in, out]

On input, this variable specifies the size of the <i>lpNameBuffer</i> buffer, in <b>TCHARs</b>. If the function is successful, the variable receives the number of <b>TCHARs</b> copied to the buffer, not including the terminating null character. 




If <i>lpNameBuffer</i> is too small, the function fails and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_MORE_DATA. This parameter receives the required buffer size, in Unicode characters (whether or not Unicode is being used), including the terminating null character.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpNameBuffer</i> buffer is too small. The <i>lpnSize</i> parameter contains the number of bytes required to receive the name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The domain controller is not available to perform the lookup

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NONE_MAPPED</b></dt>
</dl>
</td>
<td width="60%">
The user name is not available in the specified format.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/secext/ne-secext-extended_name_format">EXTENDED_NAME_FORMAT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
 

 

