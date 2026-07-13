---
UID: NF:ras.RasGetEapUserIdentityW
title: RasGetEapUserIdentityW function (ras.h)
description: The RasGetEapUserIdentity function retrieves identity information for the current user. Use this information to call RasDial with a phone-book entry that requires Extensible Authentication Protocol (EAP). (Unicode)
helpviewer_keywords: ["RASEAPF_Logon", "RASEAPF_NonInteractive", "RASEAPF_Preview", "RasGetEapUserIdentity", "RasGetEapUserIdentity function [RAS]", "RasGetEapUserIdentityW", "_ras_rasgeteapuseridentity", "ras/RasGetEapUserIdentity", "ras/RasGetEapUserIdentityW", "rras.rasgeteapuseridentity"]
old-location: rras\rasgeteapuseridentity.htm
tech.root: RRAS
ms.assetid: b1b44672-86f3-4d8b-b816-31167a84b05a
ms.date: 12/05/2018
ms.keywords: RASEAPF_Logon, RASEAPF_NonInteractive, RASEAPF_Preview, RasGetEapUserIdentity, RasGetEapUserIdentity function [RAS], RasGetEapUserIdentityA, RasGetEapUserIdentityW, _ras_rasgeteapuseridentity, ras/RasGetEapUserIdentity, ras/RasGetEapUserIdentityA, ras/RasGetEapUserIdentityW, rras.rasgeteapuseridentity
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetEapUserIdentityW (Unicode) and RasGetEapUserIdentityA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasGetEapUserIdentityW
 - ras/RasGetEapUserIdentityW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasGetEapUserIdentity
 - RasGetEapUserIdentityA
 - RasGetEapUserIdentityW
---

# RasGetEapUserIdentityW function


## -description

The 
<b>RasGetEapUserIdentity</b> function retrieves identity information for the current user. Use this information to call 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> with a phone-book entry that requires Extensible Authentication Protocol (EAP).

## -parameters

### -param pszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path of the phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the system phone book.

### -param pszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies an existing entry name.

### -param dwFlags [in]

Specifies zero or more of the following flags that qualify the authentication process.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASEAPF_NonInteractive"></a><a id="raseapf_noninteractive"></a><a id="RASEAPF_NONINTERACTIVE"></a><dl>
<dt><b>RASEAPF_NonInteractive</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the authentication protocol should not bring up a graphical user-interface. If this flag is not present, it is okay for the protocol to display a user interface.

</td>
</tr>
<tr>
<td width="40%"><a id="RASEAPF_Logon"></a><a id="raseapf_logon"></a><a id="RASEAPF_LOGON"></a><dl>
<dt><b>RASEAPF_Logon</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the user data is obtained from WinLogon.

</td>
</tr>
<tr>
<td width="40%"><a id="RASEAPF_Preview"></a><a id="raseapf_preview"></a><a id="RASEAPF_PREVIEW"></a><dl>
<dt><b>RASEAPF_Preview</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the user should be prompted for identity information before dialing.

</td>
</tr>
</table>

### -param hwnd [in]

Handle to the parent window for the UI dialog. If the <i>fInvokeUI</i> parameter is <b>FALSE</b>, then <i>hwnd</i> should be <b>NULL</b>.

### -param ppRasEapUserIdentity [out]

Pointer to a pointer that, on successful return, receives the address of the 
<a href="/previous-versions/windows/desktop/legacy/aa377247(v=vs.85)">RASEAPUSERIDENTITY</a> structure that contains EAP user identity information. 
<b>RasGetEapUserIdentity</b> allocates the memory buffer for the 
<b>RASEAPUSERIDENTITY</b> structure. Free this memory by calling 
<a href="/windows/desktop/api/ras/nf-ras-rasfreeeapuseridentitya">RasFreeEapUserIdentity</a>.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcbEapUserIdentity</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERACTIVE_MODE</b></dt>
</dl>
</td>
<td width="60%">
The function was called with the RASEAPF_NonInteractive flag. However, the authentication protocol must display a UI in order to obtain the required identity information from the user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION_FOR_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
Either the authentication method for this phone-book entry is not EAP, or the authentication method is EAP but the protocol uses the standard Windows NT/Windows 2000 credentials dialog to obtain user identity information. In either case, the caller does not need to pass EAP identity information to 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RASMAN_CANNOT_INITIALIZE</b></dt>
</dl>
</td>
<td width="60%">
The Remote Access Service failed to initialize properly.

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>

## -remarks

<b>RasGetEapUserIdentity</b> calls the RAS function 
<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuserdataa">RasGetEapUserData</a> and the EAP function 
<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetidentity">RasEapGetIdentity</a>. <b>RasEapGetIdentity</b> is implemented by the authentication protocol.

If the function succeeds, that is the return value is NO_ERROR, the caller should copy the EAP identity information from the <a href="/previous-versions/windows/desktop/legacy/aa377247(v=vs.85)">RASEAPUSERIDENTITY</a> structure pointed to by 
the <i>ppRasEapUserIdentity</i> parameter to the 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> and 
<a href="/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a> structures used in the call to 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>.

If the remote access application being developed has a graphical user interface, the caller of 
<b>RasGetEapUserIdentity</b> should not specify the RASEAPF_NonInteractive flag. If the application has a command-line user interface, the caller may want to specify the RASEAPF_NonInteractive flag to prevent the authentication protocol from displaying a graphical user interface.





> [!NOTE]
> The ras.h header defines RasGetEapUserIdentity as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377247(v=vs.85)">RASEAPUSERIDENTITY</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetidentity">RasEapGetIdentity</a>



<a href="/windows/desktop/api/ras/nf-ras-rasfreeeapuseridentitya">RasFreeEapUserIdentity</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgeteapuserdataa">RasGetEapUserData</a>



<a href="/windows/desktop/api/ras/nf-ras-rasseteapuserdataa">RasSetEapUserData</a>
