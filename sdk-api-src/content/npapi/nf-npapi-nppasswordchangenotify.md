---
UID: NF:npapi.NPPasswordChangeNotify
title: NPPasswordChangeNotify function
author: windows-sdk-content
description: MPR calls this function to notify the credential manager of a password change event.
old-location: security\nppasswordchangenotify.htm
tech.root: secauthn
ms.assetid: 5c7f5672-f379-4518-ae60-4f7d7e4caffa
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: NPPasswordChangeNotify, NPPasswordChangeNotify function [Security], SvcCtl, WN_NT_PASSWORD_CHANGED, WN_VALID_LOGON_ACCOUNT, WinSta_0, _mnp_nppasswordchangenotify, npapi/NPPasswordChangeNotify, security.nppasswordchangenotify
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
 - NPPasswordChangeNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NPPasswordChangeNotify function


## -description


MPR calls this function to notify the credential manager of a password change event. The <b>NPPasswordChangeNotify</b> function is implemented by a credential manager DLL.


## -parameters




### -param lpAuthentInfoType [in]

Pointer to a string that identifies the type of structure pointed to by <i>lpAuthentInfo</i>. 




When Microsoft is the primary authenticator, the following string is specified for interactive and service controller logons.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>MSV1_0:Interactive 
Kerberos:Interactive
</pre>
</td>
</tr>
</table></span></div>

### -param lpAuthentInfo [in]

Pointer to an structure that contains the new credentials. 




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

Pointer to a structure that contains the credentials used before the authentication information change. Prior information is provided if the user was forced to change the password (or other authentication information) before logging on. If the user was not forced to change authentication information, this pointer is <b>NULL</b>. The values expected here are the same as those in <i>lpAuthentInfo</i>. 




When Microsoft is the primary authenticator, the structure used is 
<a href="https://msdn.microsoft.com/f9b9a966-54b9-4f89-98cc-d92e3f74571d">MSV1_0_INTERACTIVE_LOGON</a> or 
<a href="https://msdn.microsoft.com/96aec0cc-b3e1-4b4b-aa0e-ecf05b9fabbe">KERB_INTERACTIVE_LOGON</a>.


### -param lpStationName [in]

Pointer to a string that specifies the name of the station the user has logged on to. The station name may be used to determine whether additional provider-specific information can be obtained. 




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
Indicates that this is a logon initiated by the service controller. <i>StationHandle</i> is not used in this case.

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
 


### -param dwChangeInfo [in]

If set, specifies a flag that provides change information. This parameter can be one of the flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WN_VALID_LOGON_ACCOUNT"></a><a id="wn_valid_logon_account"></a><dl>
<dt><b>WN_VALID_LOGON_ACCOUNT</b></dt>
</dl>
</td>
<td width="60%">
This flag indicates that the authentication information changed will affect all future logons. The user belongs to a trusted domain.

</td>
</tr>
<tr>
<td width="40%"><a id="WN_NT_PASSWORD_CHANGED"></a><a id="wn_nt_password_changed"></a><dl>
<dt><b>WN_NT_PASSWORD_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
This flag indicates that the password was changed. 




Some authentication information changes will only affect connections made in untrusted domains. These are the accounts that the user cannot use to log onto this computer anyway. In these cases, <i>dwChangeInfo</i> is not set.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the function returns WN_SUCCESS.

If the function fails, it returns an error code, which can be one of the following values.

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

<a href="https://msdn.microsoft.com/5c7f5672-f379-4518-ae60-4f7d7e4caffa">NPPasswordChangeNotify</a> is not supported.

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



The  <b>NPPasswordChangeNotify</b> function is implemented by credential managers to receive notifications when authentication information changes.

<b>Windows Server 2003 and Windows XP:  </b><b>NPPasswordChangeNotify</b> is called on a computer a user is logging into if the password has been changed somewhere else. Note that this behavior is not supported beginning with Windows Vista and Windows Server 2008.




## -see-also




<a href="https://msdn.microsoft.com/f9b9a966-54b9-4f89-98cc-d92e3f74571d">MSV1_0_INTERACTIVE_LOGON</a>



<a href="https://msdn.microsoft.com/8d399bae-4084-4f06-b7f5-036a54d8d90e">NPGetCaps</a>



<a href="https://msdn.microsoft.com/9b0e5646-ac57-4eae-bad7-a16c07b51f4b">NPLogonNotify</a>
 

 

