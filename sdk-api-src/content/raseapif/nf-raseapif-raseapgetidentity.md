---
UID: NF:raseapif.RasEapGetIdentity
title: RasEapGetIdentity function (raseapif.h)
description: The RAS connection manager calls the RasEapGetIdentity function to obtain identity information for the user requesting authentication.
helpviewer_keywords: ["RAS_EAP_FLAG_8021X_AUTH","RAS_EAP_FLAG_FIRST_LINK","RAS_EAP_FLAG_LOGON","RAS_EAP_FLAG_MACHINE_AUTH","RAS_EAP_FLAG_NON_INTERACTIVE","RAS_EAP_FLAG_PREVIEW","RAS_EAP_FLAG_ROUTER","RasEapGetIdentity","RasEapGetIdentity callback","RasEapGetIdentity callback function [EAP]","_eap_raseapgetidentity","eap.raseapgetidentity","raseapif/RasEapGetIdentity"]
old-location: eap\raseapgetidentity.htm
tech.root: EAP
ms.assetid: 66bc34d2-54b9-46eb-b952-6ad66868c8ce
ms.date: 12/05/2018
ms.keywords: RAS_EAP_FLAG_8021X_AUTH, RAS_EAP_FLAG_FIRST_LINK, RAS_EAP_FLAG_LOGON, RAS_EAP_FLAG_MACHINE_AUTH, RAS_EAP_FLAG_NON_INTERACTIVE, RAS_EAP_FLAG_PREVIEW, RAS_EAP_FLAG_ROUTER, RasEapGetIdentity, RasEapGetIdentity callback, RasEapGetIdentity callback function [EAP], _eap_raseapgetidentity, eap.raseapgetidentity, raseapif/RasEapGetIdentity
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasEapGetIdentity
 - raseapif/RasEapGetIdentity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Raseapif.h
api_name:
 - RasEapGetIdentity
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
[Multilink and Callback Connections](/windows/win32/eap/multilink-and-callback-connections) for more information.

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
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_input">PPP_EAP_INPUT</a> during the call to 
<a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a>. 




The authentication protocol should allocate the memory buffer for the identity data. RAS will free this memory by calling 
<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a>.

### -param pdwSizeOfUserDataOut [out]

Pointer to a <b>DWORD</b> variable that receives the size of the data pointed to by the <i>ppUserDataOut</i> parameter.

### -param ppwszIdentityOut [out]

Pointer to a pointer that, on successful return, points to a null-terminated Unicode string that identifies the user requesting authentication. This string is passed to the authentication protocol in the <b>pszIdentity</b> member of 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_input">PPP_EAP_INPUT</a> during the call to 
<a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function was not able to allocate memory for the user data, the return value should be <b>ERROR_NOT_ENOUGH_MEMORY</b>.

If the function is called with the RAS_EAP_FLAG_NON_INTERACTIVE flag, but must invoke a user interface to determine the user's identity, the function should return <b>ERROR_INTERACTIVE_MODE</b>.

If the function fails in some other way, the return value should be an appropriate error code from Winerror.h, Raserror.h, or Mprerror.h.

## -remarks

The DLL that implements 
<b>RasEapGetIdentity</b> and 
<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a> may support more than one authentication protocol. The <i>dwEapTypeId</i> parameter specifies for which protocol to invoke the identity user interface.

The IEEE 802.1X and PPP protocols do not call 
<b>RasEapGetIdentity</b> without an implementation of 
<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a>.

The authentication protocol receives the data returned from 
<b>RasEapGetIdentity</b> in the <b>pUserData</b> member of 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_input">PPP_EAP_INPUT</a> during 
<a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a>. To store the data for this user in the registry, the authentication protocol should set the <b>pUserData</b> member of 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_output">PPP_EAP_OUTPUT</a> to point to the data, and the <b>fSaveUserData</b> member of 
<b>PPP_EAP_OUTPUT</b> to <b>TRUE</b>.

This function is called by the RAS function, 
<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuseridentitya">RasGetEapUserIdentity</a>.

If 
<b>RasEapGetIdentity</b> displays a user interface, the user interface must support 
<a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> messages where 
<a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a>(<i>wParam</i>) equals IDCANCEL.

## -see-also

[EAP Functions](/windows/win32/eap/eap-functions)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



[Obtaining Identity Information](/windows/win32/eap/obtaining-identity-information)



<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_input">PPP_EAP_INPUT</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a>



<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuseridentitya">RasGetEapUserIdentity</a>