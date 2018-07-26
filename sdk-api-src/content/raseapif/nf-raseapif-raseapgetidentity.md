---
UID: NF:raseapif.RasEapGetIdentity
title: RasEapGetIdentity function
author: windows-sdk-content
description: The RAS connection manager calls the RasEapGetIdentity function to obtain identity information for the user requesting authentication.
old-location: eap\raseapgetidentity.htm
old-project: eap
ms.assetid: 66bc34d2-54b9-46eb-b952-6ad66868c8ce
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: RAS_EAP_FLAG_8021X_AUTH, RAS_EAP_FLAG_FIRST_LINK, RAS_EAP_FLAG_LOGON, RAS_EAP_FLAG_MACHINE_AUTH, RAS_EAP_FLAG_NON_INTERACTIVE, RAS_EAP_FLAG_PREVIEW, RAS_EAP_FLAG_ROUTER, RasEapGetIdentity, RasEapGetIdentity callback, RasEapGetIdentity callback function [EAP], _eap_raseapgetidentity, eap.raseapgetidentity, raseapif/RasEapGetIdentity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: raseapif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RAS_AUTH_ATTRIBUTE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Raseapif.h
api_name:
 - RasEapGetIdentity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# RasEapGetIdentity function


## -description


The RAS connection manager calls the 
<b>RasEapGetIdentity</b> function to obtain identity information for the user requesting authentication.


## -parameters




### -param dwEapTypeId [in]

Specifies the authentication protocol for which to invoke the identity user interface.


### -param hwndParent [in]

Handle to the parent window for the user interface dialog. If the <i>dwFlags</i> parameter contains the RAS_EAP_FLAG_NON_INTERACTIVE flag, then <i>hwndParent</i> is <b>NULL</b>.


### -param dwFlags [in]

Specifies zero or more of the following flags that qualify the authentication process.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_ROUTER"></a><a id="ras_eap_flag_router"></a><dl>
<dt><b>RAS_EAP_FLAG_ROUTER</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the computer that is dialing in is a router. The absence of this flag indicates that the computer dialing in is a RAS client.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_NON_INTERACTIVE"></a><a id="ras_eap_flag_non_interactive"></a><dl>
<dt><b>RAS_EAP_FLAG_NON_INTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the authentication protocol should not bring up a user-interface. If the authentication protocol is not able to determine the identity from the data supplied, it should return the error code, <b>ERROR_INTERACTIVE_MODE</b>. If this flag is specified, the <i>hwndParent</i> parameter will be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_LOGON"></a><a id="ras_eap_flag_logon"></a><dl>
<dt><b>RAS_EAP_FLAG_LOGON</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the user data is obtained when logging onto the local system, that is from Winlogon.exe.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_PREVIEW"></a><a id="ras_eap_flag_preview"></a><dl>
<dt><b>RAS_EAP_FLAG_PREVIEW</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the user should be prompted for identity information before dialing.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_FIRST_LINK"></a><a id="ras_eap_flag_first_link"></a><dl>
<dt><b>RAS_EAP_FLAG_FIRST_LINK</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this connection is the first link in a multilink connection. See 
<a href="https://msdn.microsoft.com/a6aee73b-43b2-43b4-a6f1-ac7b293c44ad">Multilink and Callback Connections</a> for more information.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_MACHINE_AUTH"></a><a id="ras_eap_flag_machine_auth"></a><dl>
<dt><b>RAS_EAP_FLAG_MACHINE_AUTH</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the authentication process use machine credentials for authentication. The credentials can be a certificate, machine name/password as in the case of MSCHAPv2 or any other means of identifying the machine. If the authentication protocol does not support machine authentication, it should return the error <b>ERROR_NOT_SUPPORTED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_8021X_AUTH"></a><a id="ras_eap_flag_8021x_auth"></a><dl>
<dt><b>RAS_EAP_FLAG_8021X_AUTH</b></dt>
</dl>
</td>
<td width="60%">
Specifies that this session is executing in a wireless context.

</td>
</tr>
</table>
 


### -param pwszPhonebook [in]

Pointer to a null-terminated Unicode string that specifies the full path of the phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the system phone book.


### -param pwszEntry [in]

Pointer to a null-terminated Unicode string that specifies an existing entry name.


### -param pConnectionDataIn [in]

Pointer to the connection-specific data currently stored in the phone-book entry.


### -param dwSizeOfConnectionDataIn [in]

Specifies the size of the connection-specific data currently stored in the phone-book entry.


### -param pUserDataIn [in]

Pointer to the user-specific data currently stored for this user in the registry.


### -param dwSizeOfUserDataIn [in]

Specifies the size of the user-specific data currently stored for this user in the registry.


### -param ppUserDataOut [out]

Pointer to a pointer that, on successful return, points to the identity data for the user. This data will be passed to the authentication protocol in the <b>pUserData</b> member of 
<a href="https://msdn.microsoft.com/80a8f118-323d-4040-91f7-202eeee6d227">PPP_EAP_INPUT</a> during the call to 
<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a>. 




The authentication protocol should allocate the memory buffer for the identity data. RAS will free this memory by calling 
<a href="https://msdn.microsoft.com/d6eb6afd-0d92-4050-b6a9-7bd90788e01c">RasEapFreeMemory</a>.


### -param pdwSizeOfUserDataOut [out]

Pointer to a <b>DWORD</b> variable that receives the size of the data pointed to by the <i>ppUserDataOut</i> parameter.


### -param ppwszIdentityOut

TBD




#### - ppwszIdentity [out]

Pointer to a pointer that, on successful return, points to a null-terminated Unicode string that identifies the user requesting authentication. This string is passed to the authentication protocol in the <b>pszIdentity</b> member of 
<a href="https://msdn.microsoft.com/80a8f118-323d-4040-91f7-202eeee6d227">PPP_EAP_INPUT</a> during the call to 
<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a>.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function was not able to allocate memory for the user data, the return value should be <b>ERROR_NOT_ENOUGH_MEMORY</b>.

If the function is called with the RAS_EAP_FLAG_NON_INTERACTIVE flag, but must invoke a user interface to determine the user's identity, the function should return <b>ERROR_INTERACTIVE_MODE</b>.

If the function fails in some other way, the return value should be an appropriate error code from Winerror.h, Raserror.h, or Mprerror.h.




## -remarks



The DLL that implements 
<b>RasEapGetIdentity</b> and 
<a href="https://msdn.microsoft.com/d6eb6afd-0d92-4050-b6a9-7bd90788e01c">RasEapFreeMemory</a> may support more than one authentication protocol. The <i>dwEapTypeId</i> parameter specifies for which protocol to invoke the identity user interface.

The IEEE 802.1X and PPP protocols do not call 
<b>RasEapGetIdentity</b> without an implementation of 
<a href="https://msdn.microsoft.com/d6eb6afd-0d92-4050-b6a9-7bd90788e01c">RasEapFreeMemory</a>.

The authentication protocol receives the data returned from 
<b>RasEapGetIdentity</b> in the <b>pUserData</b> member of 
<a href="https://msdn.microsoft.com/80a8f118-323d-4040-91f7-202eeee6d227">PPP_EAP_INPUT</a> during 
<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a>. To store the data for this user in the registry, the authentication protocol should set the <b>pUserData</b> member of 
<a href="https://msdn.microsoft.com/d1634973-f6af-4be3-914a-513098c5fccf">PPP_EAP_OUTPUT</a> to point to the data, and the <b>fSaveUserData</b> member of 
<b>PPP_EAP_OUTPUT</b> to <b>TRUE</b>.

This function is called by the RAS function, 
<a href="https://msdn.microsoft.com/b1b44672-86f3-4d8b-b816-31167a84b05a">RasGetEapUserIdentity</a>.

If 
<b>RasEapGetIdentity</b> displays a user interface, the user interface must support 
<a href="_win32_wm_command_cpp">WM_COMMAND</a> messages where 
<a href="_win32_loword_cpp">LOWORD</a>(<i>wParam</i>) equals IDCANCEL.




## -see-also




<a href="https://msdn.microsoft.com/090a3620-3732-4466-95ac-ce9cbdd36484">EAP Functions</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/773c9fdb-c810-4cea-afed-df6484a9c9c9">Obtaining Identity Information</a>



<a href="https://msdn.microsoft.com/80a8f118-323d-4040-91f7-202eeee6d227">PPP_EAP_INPUT</a>



<a href="https://msdn.microsoft.com/d6eb6afd-0d92-4050-b6a9-7bd90788e01c">RasEapFreeMemory</a>



<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>



<a href="https://msdn.microsoft.com/b1b44672-86f3-4d8b-b816-31167a84b05a">RasGetEapUserIdentity</a>
 

 

