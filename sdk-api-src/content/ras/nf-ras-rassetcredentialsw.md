---
UID: NF:ras.RasSetCredentialsW
title: RasSetCredentialsW function
author: windows-sdk-content
description: Sets the user credentials associated with a specified RAS phone-book entry.
old-location: rras\rassetcredentials.htm
tech.root: rras
ms.assetid: 5ebfffb7-9158-4414-982c-e187600aa1ab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RasSetCredentials, RasSetCredentials function [RAS], RasSetCredentialsA, RasSetCredentialsW, _ras_rassetcredentials, ras/RasSetCredentials, ras/RasSetCredentialsA, ras/RasSetCredentialsW, rras.rassetcredentials
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
req.unicode-ansi: RasSetCredentialsW (Unicode) and RasSetCredentialsA (ANSI)
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
 - RasSetCredentials
 - RasSetCredentialsA
 - RasSetCredentialsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasSetCredentialsW function


## -description


The <b>RasSetCredentials</b> function sets the 
    user credentials associated with a specified RAS phone-book entry.


## -parameters




### -param arg1 [in]

A pointer to a null-terminated string that specifies the full path and file name of a phone-book 
      (PBK) file. If this parameter is <b>NULL</b>, the function uses the current 
      default phone-book file. The default phone-book file is the one selected by the user in the 
      <b>User Preferences</b> property sheet of the 
      <b>Dial-Up Networking</b> dialog box.


### -param arg2 [in]

A pointer to a null-terminated string that specifies the name of a phone-book entry.


### -param arg3 [in]

A pointer to a <a href="https://msdn.microsoft.com/5283b35a-adcf-4573-8c6b-5996d4e9440c">RASCREDENTIALS</a> structure that 
      specifies the user credentials to set for the specified phone-book entry. Before calling 
      <b>RasSetCredentials</b>, set the 
      <b>dwSize</b> member of the structure to 
      <code>sizeof(RASCREDENTIALS)</code> and set the <b>dwMask</b> 
      member to indicate the credential information to be set.


### -param arg4 [in]

A value that specifies whether 
      <b>RasSetCredentials</b> clears existing credentials by 
      setting them to the empty string, "". If this flag is <b>TRUE</b>, the 
      <b>dwMask</b> member of the 
      <a href="https://msdn.microsoft.com/5283b35a-adcf-4573-8c6b-5996d4e9440c">RASCREDENTIALS</a> structure indicates which 
      credentials that the function sets to the empty string. If this flag is <b>FALSE</b>, the 
      function sets the indicated credentials according to the contents of their corresponding 
      <b>RASCREDENTIALS</b> members.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from 
       <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> 
       or WinError.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
The specified phone book cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpCredentials</i> parameter was <b>NULL</b>, or the 
        specified entry does not exist in the phone book.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
One of the following conditions occurred:
        

<ul>
<li>The calling application attempted to set default credentials for a per-user connection. Default 
          credentials can be set only for an all-user connection.</li>
<li>The user does not have the correct privileges to set pre-shared keys or credentials for all users in 
          case of all-user connectoids.  Only administrators can complete these tasks.</li>
</ul>
</td>
</tr>
</table>
 




## -remarks



The <b>RasSetCredentials</b> function sets the user 
    credentials associated with a specified RAS phone-book entry. The credentials stored with a phone-book entry are 
    the credentials of the last user to successfully connect by using the specified phone-book entry, or the 
    credentials subsequently specified in a call to the 
    <b>RasSetCredentials</b> or 
    <a href="https://msdn.microsoft.com/e1acd68e-796e-49a2-8c7d-c0fd1a9764ef">RasSetEntryDialParams</a> function for the 
    phone-book entry.

The <b>RasSetCredentials</b> function is the preferred 
    way of securely storing credentials with a phone-book entry. 
    <b>RasSetCredentials</b> supersedes the 
    <a href="https://msdn.microsoft.com/e1acd68e-796e-49a2-8c7d-c0fd1a9764ef">RasSetEntryDialParams</a> function, which may not be 
    supported in future releases of the Windows operating system.

A password handle is "****************" (16 asterisks). If you call 
    <a href="https://msdn.microsoft.com/37b67845-dd9f-4adc-a33a-f0e5c0bdb6f7">RasGetCredentials</a> and receive 16 *s back in the 
    password field, you have a stored password and, for security reasons, it will not be given  back to you in plain 
    text.  If the <b>szPassword</b> member of the 
    <a href="https://msdn.microsoft.com/5283b35a-adcf-4573-8c6b-5996d4e9440c">RASCREDENTIALS</a> structure contains the password handle 
    (16 *s) returned by <b>RasGetCredentials</b> or 
    <a href="https://msdn.microsoft.com/c6752f95-c7e8-44d9-9dbd-9f03cc4778fa">RasGetEntryDialParams</a>,  the next call to 
    <b>RasSetCredentials</b> will not change the saved 
    password.

To set the default credentials for an all-user connection, set the 
    <b>RASCM_DefaultCreds</b> flag in the <b>dwMask</b> member of the 
    <a href="https://msdn.microsoft.com/5283b35a-adcf-4573-8c6b-5996d4e9440c">RASCREDENTIALS</a> structure pointed to by 
    the <i>lpCredentials</i> parameter. If you attempt to set default credentials for a per-user 
    connection, <b>RasSetCredentials</b> returns 
    <b>ERROR_ACCESS_DENIED</b>. 

When setting credentials for an all-users connection, if 
    the calling application specifies a non-NULL value for the phone-book parameter, 
    <i>lpszPhonebook</i>, the phone-book file must be located in the phone-book directory beneath 
    the all-users application data path. To obtain the correct location for the phone-book file, first call 
    <a href="_win32_shgetfolderpath_cpp">SHGetFolderPath</a> with a 
    <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value of <b>CSIDL_COMMON_APPDATA</b>. 
    <b>SHGetFolderPath</b> returns the all-users 
    application data path. Append the following string to this path:

Microsoft\Network\Connections\Pbk

The combined path is the correct location for the phone-book file.

<div class="alert"><b>Note</b>  Specifying a non-NULL value for the <i>lpszPhonebook</i> parameter may not be supported in 
    later versions of the Windows operating system.</div>
<div> </div>
To set a pre-shared key, use the <b>RASCM_PreSharedKey</b> flag in the 
    <a href="https://msdn.microsoft.com/5283b35a-adcf-4573-8c6b-5996d4e9440c">RASCREDENTIALS</a>.<b>dwMask</b> 
    field.




## -see-also




<a href="https://msdn.microsoft.com/5283b35a-adcf-4573-8c6b-5996d4e9440c">RASCREDENTIALS</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/37b67845-dd9f-4adc-a33a-f0e5c0bdb6f7">RasGetCredentials</a>



<a href="https://msdn.microsoft.com/e1acd68e-796e-49a2-8c7d-c0fd1a9764ef">RasSetEntryDialParams</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

