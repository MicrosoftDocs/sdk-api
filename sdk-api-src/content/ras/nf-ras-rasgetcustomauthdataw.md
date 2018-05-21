---
UID: NF:ras.RasGetCustomAuthDataW
title: RasGetCustomAuthDataW function
author: windows-driver-content
description: Use the RasGetCustomAuthData function to retrieve connection-specific authentication information. This information is not specific to a particular user.
old-location: rras\rasgetcustomauthdata.htm
old-project: RRAS
ms.assetid: 626d372c-4da8-4c79-92dd-9cc5b4b8a618
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: RasGetCustomAuthData, RasGetCustomAuthData function [RAS], RasGetCustomAuthDataA, RasGetCustomAuthDataW, _ras_rasgetcustomauthdata, ras/RasGetCustomAuthData, ras/RasGetCustomAuthDataA, ras/RasGetCustomAuthDataW, rras.rasgetcustomauthdata
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
req.unicode-ansi: RasGetCustomAuthDataW (Unicode) and RasGetCustomAuthDataA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RASPROJECTION_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rasapi32.dll
api_name:
-	RasGetCustomAuthData
-	RasGetCustomAuthDataA
-	RasGetCustomAuthDataW
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RasGetCustomAuthDataW function


## -description


Use the 
<b>RasGetCustomAuthData</b> function to retrieve connection-specific authentication information. This information is not specific to a particular user.


## -parameters




### -param pszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path of the phone-book (PBK) file. If this parameter is <b>NULL</b>, the function  uses the system phone book.


### -param pszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies an existing entry name.


### -param pbCustomAuthData [out]

Pointer to a buffer that receives the authentication data. The caller should allocate the memory for this buffer. If the buffer is not large enough, 
<b>RasGetCustomAuthData</b>  returns ERROR_BUFFER_TOO_SMALL, and the <i>pdwSizeofEapData</i> parameter  contains the required size.


### -param pdwSizeofCustomAuthData [in, out]

Pointer to a <b>DWORD</b> variable that, on input, specifies the size of the buffer pointed to by the <i>pbCustomAuthData</i> parameter. 




If the buffer specified by the <i>pbCustomAuthData</i> parameter is not large enough, <i>pdwSizeofEapData</i> receives, on output, the required size.


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
The <i>pdwSizeofCustomAuthData</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>pbCustomAuthData</i> is too small to receive the data. The <i>pdwSizeofCustomAuthData</i> contains the required size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/6b1a1c73-28af-43ff-b79c-c796ddae219c">RasGetEapUserData</a> was unable to open the specified phone-book file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/6b1a1c73-28af-43ff-b79c-c796ddae219c">RasGetEapUserData</a> was unable to find the specified entry in the phone book.

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




<a href="https://msdn.microsoft.com/6b1a1c73-28af-43ff-b79c-c796ddae219c">RasGetEapUserData</a>



<a href="https://msdn.microsoft.com/a3369537-1b46-4d7b-8ee1-f6965a3f296d">RasSetCustomAuthData</a>
 

 

