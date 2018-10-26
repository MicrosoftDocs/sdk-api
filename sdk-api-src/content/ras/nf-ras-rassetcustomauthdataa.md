---
UID: NF:ras.RasSetCustomAuthDataA
title: RasSetCustomAuthDataA function
author: windows-sdk-content
description: Use the RasSetCustomAuthData function to set connection-specific authentication information. This information should not be specific to a particular user.
old-location: rras\rassetcustomauthdata.htm
tech.root: rras
ms.assetid: a3369537-1b46-4d7b-8ee1-f6965a3f296d
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: RasSetCustomAuthData, RasSetCustomAuthData function [RAS], RasSetCustomAuthDataA, RasSetCustomAuthDataW, _ras_rassetcustomauthdata, ras/RasSetCustomAuthData, ras/RasSetCustomAuthDataA, ras/RasSetCustomAuthDataW, rras.rassetcustomauthdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasSetCustomAuthDataW (Unicode) and RasSetCustomAuthDataA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasSetCustomAuthData
 - RasSetCustomAuthDataA
 - RasSetCustomAuthDataW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasSetCustomAuthDataA function


## -description


Use the 
<b>RasSetCustomAuthData</b> function to set connection-specific authentication information. This information should not be specific to a particular user.


## -parameters




### -param pszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path of the phone-book (PBK) file. If this parameter is <b>NULL</b>, the function  uses the system phone book.


### -param pszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies an existing entry name.


### -param pbCustomAuthData [in]

Pointer to a buffer that specifies the new authentication data.


### -param dwSizeofCustomAuthData [in]

Specifies the size of the data pointed to by the <i>pbCustomAuthData</i> parameter.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSizeofCustomAuthData</i> parameter is zero, or the <i>pbCustomAuthData</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/702e5c42-cc8c-43cf-a0bf-d3e450c031a4">RasSetEapUserData</a> was unable to open the specified phone-book file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/702e5c42-cc8c-43cf-a0bf-d3e450c031a4">RasSetEapUserData</a> was unable to find the specified entry in the phone book.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/626d372c-4da8-4c79-92dd-9cc5b4b8a618">RasGetCustomAuthData</a>



<a href="https://msdn.microsoft.com/702e5c42-cc8c-43cf-a0bf-d3e450c031a4">RasSetEapUserData</a>
 

 

