---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MsiGetProductInfoFromScriptW function


## -description



			The 
<b>MsiGetProductInfoFromScript</b> function returns product information for a Windows Installer script file.


## -parameters




### -param szScriptFile [in]

A null-terminated string specifying the full path to the script file. The script file is the advertise script that was created by calling <a href="https://msdn.microsoft.com/b28736cb-7097-4f6e-a158-a525a32d9b58">MsiAdvertiseProduct</a> or <a href="https://msdn.microsoft.com/27e8deb6-912f-4103-97a6-ec505340dccc">MsiAdvertiseProductEx</a>.


### -param lpProductBuf39 [out]

Points to a buffer that receives the product code. The buffer must be 39 characters long. The first 38 characters are for the product code 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>, and the last character is for the terminating null character.


### -param plgidLanguage [out]

Points to a variable that receives the product language.


### -param pdwVersion [out]

Points to a buffer that receives the product version.


### -param lpNameBuf [out]

Points to a buffer that receives the product name. The buffer includes a terminating null character.


### -param pcchNameBuf [in, out]

Points to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpNameBuf</i> parameter. This size should include the terminating null character. When the function returns, this variable contains the length of the string stored in the buffer. The count returned does not include the terminating null character. If the buffer is not large enough, the function returns ERROR_MORE_DATA, and the variable contains the size of the string in characters, without counting the null character.


### -param lpPackageBuf [out]

Points to a buffer that receives the package name. The buffer includes the terminating null character.


### -param pcchPackageBuf [in, out]

Points to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpPackageNameBuf</i> parameter. This size should include the terminating null character. When the function returns, this variable contains the length of the string stored in the buffer. The count returned does not include the terminating null character. If the buffer is not large enough, the function returns ERROR_MORE_DATA, and the variable contains the size of the string in characters, without counting the null character.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer was too small to hold the entire value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Could not get script information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This function is only available on Windows 2000 and Windows XP.

</td>
</tr>
</table>
 



