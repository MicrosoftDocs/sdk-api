---
UID: NF:npapi.NPLogonNotify
title: NPLogonNotify function
author: windows-sdk-content
description: MPR calls this function to notify the credential manager that a logon event has occurred, allowing the credential manager to return a logon script.
old-location: security\nplogonnotify.htm
tech.root: secauthn
ms.assetid: 9b0e5646-ac57-4eae-bad7-a16c07b51f4b
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: NPLogonNotify, NPLogonNotify function [Security], SvcCtl, WinSta_0, _mnp_nplogonnotify, npapi/NPLogonNotify, security.nplogonnotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: npapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPLogonNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NPLogonNotify function


## -description


MPR calls this function to notify the credential manager that a logon event has occurred, allowing the credential manager to return a logon script. The <b>NPLogonNotify</b> function is implemented by a credential manager DLL (see Remarks).


## -parameters




### -param lpLogonId [in]

Pointer to the identifier of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session</a> that just logged on.


### -param lpAuthentInfoType [in]

Pointer to a string that identifies the type of structure pointed to by <i>lpAuthentInfo</i>. 




When Microsoft is the primary authenticator, one of the following strings is specified for interactive and service controller logons.

<pre class="syntax" xml:space="preserve"><code>MSV1_0:Interactive
Kerberos:Interactive
</code></pre>

### -param lpAuthentInfo [in]

Pointer to a structure that contains the credentials used to successfully log the user on through the primary authenticator. 




When Microsoft is the primary authenticator (that is, when <i>lpAuthentifoType</i> is "MSV1_0:Interactive" or "Kerberos:Interactive"), the structure used is 
<a href="https://msdn.microsoft.com/f9b9a966-54b9-4f89-98cc-d92e3f74571d">MSV1_0_INTERACTIVE_LOGON</a> or 
<a href="https://msdn.microsoft.com/96aec0cc-b3e1-4b4b-aa0e-ecf05b9fabbe">KERB_INTERACTIVE_LOGON</a>.


### -param lpPreviousAuthentInfoType [in]

Pointer to a string that identifies the type of structure pointed to by <i>lpPreviousAuthentInfo</i>. If the pointer is <b>NULL</b>, there was no previous information. The values that are expected here are the same as those in <i>lpAuthentInfoType</i>. 




When Microsoft is the primary authenticator, the following string is specified for interactive and service controller logons.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>MSV1_0:Interactive
</pre>
</td>
</tr>
</table></span></div>

### -param lpPreviousAuthentInfo [in]

Pointer to a structure that contains the credentials used before the authentication information change. Prior information is provided if the user was forced to change the password (or other authentication information) before logging on. If the user was not forced to change authentication information, this pointer is <b>NULL</b>. The values that are expected here are the same as those in <i>lpAuthentInfo</i>. 




When Microsoft is the primary authenticator, the structure used is 
<a href="https://msdn.microsoft.com/f9b9a966-54b9-4f89-98cc-d92e3f74571d">MSV1_0_INTERACTIVE_LOGON</a> or 
<a href="https://msdn.microsoft.com/96aec0cc-b3e1-4b4b-aa0e-ecf05b9fabbe">KERB_INTERACTIVE_LOGON</a>.


### -param lpStationName [in]

Pointer to a string that specifies the name of the station that the user has logged on to. The station name may be used to determine whether additional (provider-specific) information can be obtained. 




When Microsoft is the primary authenticator, one of the following strings will be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WinSta_0"></a><a id="winsta_0"></a><a id="WINSTA_0"></a><dl>
<dt><b>WinSta_0</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this is an interactive logon through the window station. In this case, <i>StationHandle</i> is an <b>HWND</b> to the parent dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="SvcCtl"></a><a id="svcctl"></a><a id="SVCCTL"></a><dl>
<dt><b>SvcCtl</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this is a logon initiated by the Service controller. <i>StationHandle</i> is not used in this case.

</td>
</tr>
</table>
 


### -param StationHandle [in]

A 32-bit value whose meaning is dependent upon the name (and consequently, the type) of the station specified in <i>lpStationName</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WinSta_0"></a><a id="winsta_0"></a><a id="WINSTA_0"></a><dl>
<dt><b>WinSta_0</b></dt>
</dl>
</td>
<td width="60%">
A handle to the owner dialog box (hwndOwner) currently displayed on the screen.

</td>
</tr>
<tr>
<td width="40%"><a id="SvcCtl"></a><a id="svcctl"></a><a id="SVCCTL"></a><dl>
<dt><b>SvcCtl</b></dt>
</dl>
</td>
<td width="60%">
Random data. Do not use.

</td>
</tr>
</table>
 


### -param lpLogonScript [out]

Pointer to a location where a pointer to a <b>null</b>-terminated string may be returned. 




After the function completes, this value may point to a <b>null</b>-terminated string that contains the name of a program to execute plus any parameters the program requires. 
<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> should be used to allocate the memory for the returned string. This memory will be freed by MPR when it is no longer needed.


## -returns



If the function succeeds, the function returns WN_SUCCESS.

If the function fails, it returns an error code, which can be one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/9b0e5646-ac57-4eae-bad7-a16c07b51f4b">NPLogonNotify</a> is not supported by the credential manager.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_FUNCTION_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The credential manager is still initializing and is not ready to be called.

</td>
</tr>
</table>
 




## -remarks



The  <b>NPLogonNotify</b> function is implemented by credential managers to receive notifications when authentication information changes.

Each credential manager is allowed to return a single command-line string that can be used to execute a logon script (the implementation should not call <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> or load a user profile directly). The buffer of this string is allocated by the credential manager. MPR is responsible for freeing it. The string returned in <i>lpLogonScript</i> should contain all the information necessary to run the script as a command line passed to 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>.

If the string requires the command processor to process the string, as in the case of commands or batch files, then the string should be prefixed with <b>cmd /C</b>.

Logon scripts will be run in the user context when the user profile is available. However, environment variables that are set will not be global and will not be available to the initial shell (for example, Program Manager) or any other program run on behalf of the user.




## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>



<a href="https://msdn.microsoft.com/f9b9a966-54b9-4f89-98cc-d92e3f74571d">MSV1_0_INTERACTIVE_LOGON</a>



<a href="https://msdn.microsoft.com/8d399bae-4084-4f06-b7f5-036a54d8d90e">NPGetCaps</a>



<a href="https://msdn.microsoft.com/5c7f5672-f379-4518-ae60-4f7d7e4caffa">NPPasswordChangeNotify</a>
 

 

