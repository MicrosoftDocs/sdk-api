---
UID: NF:npapi.NPLogonNotify
title: NPLogonNotify function (npapi.h)
description: MPR calls this function to notify the credential manager that a logon event has occurred, allowing the credential manager to return a logon script.
helpviewer_keywords: ["NPLogonNotify","NPLogonNotify function [Security]","SvcCtl","WinSta_0","_mnp_nplogonnotify","npapi/NPLogonNotify","security.nplogonnotify"]
old-location: security\nplogonnotify.htm
tech.root: security
ms.assetid: 9b0e5646-ac57-4eae-bad7-a16c07b51f4b
ms.date: 09/17/2020
ms.keywords: NPLogonNotify, NPLogonNotify function [Security], SvcCtl, WinSta_0, _mnp_nplogonnotify, npapi/NPLogonNotify, security.nplogonnotify
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPLogonNotify
 - npapi/NPLogonNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPLogonNotify
---

# NPLogonNotify function




## -description

> [!NOTE]
> This API has been deprecated and will be removed in a future release.

MPR calls this function to notify the credential manager that a logon event has occurred, allowing the credential manager to return a logon script. The <b>NPLogonNotify</b> function is implemented by a credential manager DLL (see Remarks).

## -parameters

### -param lpLogonId [in]

Pointer to the identifier of the <a href="/windows/desktop/SecGloss/s-gly">session</a> that just logged on.

### -param lpAuthentInfoType [in]

Pointer to a string that identifies the type of structure pointed to by <i>lpAuthentInfo</i>. 




When Microsoft is the primary authenticator, one of the following strings is specified for interactive and service controller logons.


``` syntax
MSV1_0:Interactive
Kerberos:Interactive

```


### -param lpAuthentInfo [in]

Pointer to a structure that contains the credentials used to successfully log the user on through the primary authenticator. 




When Microsoft is the primary authenticator (that is, when <i>lpAuthentifoType</i> is "MSV1_0:Interactive" or "Kerberos:Interactive"), the structure used is 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-msv1_0_interactive_logon">MSV1_0_INTERACTIVE_LOGON</a> or 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon">KERB_INTERACTIVE_LOGON</a>.

### -param lpPreviousAuthentInfoType [in]

Pointer to a string that identifies the type of structure pointed to by <i>lpPreviousAuthentInfo</i>. If the pointer is <b>NULL</b>, there was no previous information. The values that are expected here are the same as those in <i>lpAuthentInfoType</i>. 




When Microsoft is the primary authenticator, the following string is specified for interactive and service controller logons.


```cpp
MSV1_0:Interactive

```

### -param lpPreviousAuthentInfo [in]

Pointer to a structure that contains the credentials used before the authentication information change. Prior information is provided if the user was forced to change the password (or other authentication information) before logging on. If the user was not forced to change authentication information, this pointer is <b>NULL</b>. The values that are expected here are the same as those in <i>lpAuthentInfo</i>. 




When Microsoft is the primary authenticator, the structure used is 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-msv1_0_interactive_logon">MSV1_0_INTERACTIVE_LOGON</a> or 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon">KERB_INTERACTIVE_LOGON</a>.

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
<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> should be used to allocate the memory for the returned string. This memory will be freed by MPR when it is no longer needed.

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

<a href="/windows/desktop/api/npapi/nf-npapi-nplogonnotify">NPLogonNotify</a> is not supported by the credential manager.

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

Each credential manager is allowed to return a single command-line string that can be used to execute a logon script (the implementation should not call <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> or load a user profile directly). The buffer of this string is allocated by the credential manager. MPR is responsible for freeing it. The string returned in <i>lpLogonScript</i> should contain all the information necessary to run the script as a command line passed to 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

If the string requires the command processor to process the string, as in the case of commands or batch files, then the string should be prefixed with <b>cmd /C</b>.

Logon scripts will be run in the user context when the user profile is available. However, environment variables that are set will not be global and will not be available to the initial shell (for example, Program Manager) or any other program run on behalf of the user.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-msv1_0_interactive_logon">MSV1_0_INTERACTIVE_LOGON</a>



<a href="/windows/desktop/api/npapi/nf-npapi-npgetcaps">NPGetCaps</a>



<a href="/windows/desktop/api/npapi/nf-npapi-nppasswordchangenotify">NPPasswordChangeNotify</a>
