---
UID: NF:ras.RasGetEapUserIdentityW
title: RasGetEapUserIdentityW function
author: windows-sdk-content
description: The RasGetEapUserIdentity function retrieves identity information for the current user. Use this information to call RasDial with a phone-book entry that requires Extensible Authentication Protocol (EAP).
old-location: rras\rasgeteapuseridentity.htm
old-project: rras
ms.assetid: b1b44672-86f3-4d8b-b816-31167a84b05a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RASEAPF_Logon, RASEAPF_NonInteractive, RASEAPF_Preview, RasGetEapUserIdentity, RasGetEapUserIdentity function [RAS], RasGetEapUserIdentityA, RasGetEapUserIdentityW, _ras_rasgeteapuseridentity, ras/RasGetEapUserIdentity, ras/RasGetEapUserIdentityA, ras/RasGetEapUserIdentityW, rras.rasgeteapuseridentity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ras.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RASPROJECTION_INFO_TYPE
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
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: ADAM
---

# RasGetEapUserIdentityW function


## -description


The 
<b>RasGetEapUserIdentity</b> function retrieves identity information for the current user. Use this information to call 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> with a phone-book entry that requires Extensible Authentication Protocol (EAP).


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
<a href="https://msdn.microsoft.com/6e27d6cf-65bd-459f-ab4a-2177a2a39ff3">RASEAPUSERIDENTITY</a> structure that contains EAP user identity information. 
<b>RasGetEapUserIdentity</b> allocates the memory buffer for the 
<b>RASEAPUSERIDENTITY</b> structure. Free this memory by calling 
<a href="https://msdn.microsoft.com/84102fdc-b44a-415e-b67e-58c82e662a23">RasFreeEapUserIdentity</a>.


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
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>.

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
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -remarks



<b>RasGetEapUserIdentity</b> calls the RAS function 
<a href="https://msdn.microsoft.com/6b1a1c73-28af-43ff-b79c-c796ddae219c">RasGetEapUserData</a> and the EAP function 
<a href="_eap_raseapgetidentity">RasEapGetIdentity</a>. <b>RasEapGetIdentity</b> is implemented by the authentication protocol.

If the function succeeds, that is the return value is NO_ERROR, the caller should copy the EAP identity information from the <a href="https://msdn.microsoft.com/6e27d6cf-65bd-459f-ab4a-2177a2a39ff3">RASEAPUSERIDENTITY</a> structure pointed to by 
the <i>ppRasEapUserIdentity</i> parameter to the 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> and 
<a href="https://msdn.microsoft.com/533c9ab4-69d0-492d-81c6-2c07ca219fc7">RASDIALEXTENSIONS</a> structures used in the call to 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>.

If the remote access application being developed has a graphical user interface, the caller of 
<b>RasGetEapUserIdentity</b> should not specify the RASEAPF_NonInteractive flag. If the application has a command-line user interface, the caller may want to specify the RASEAPF_NonInteractive flag to prevent the authentication protocol from displaying a graphical user interface.




## -see-also




<a href="https://msdn.microsoft.com/6e27d6cf-65bd-459f-ab4a-2177a2a39ff3">RASEAPUSERIDENTITY</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="_eap_raseapgetidentity">RasEapGetIdentity</a>



<a href="https://msdn.microsoft.com/84102fdc-b44a-415e-b67e-58c82e662a23">RasFreeEapUserIdentity</a>



<a href="https://msdn.microsoft.com/6b1a1c73-28af-43ff-b79c-c796ddae219c">RasGetEapUserData</a>



<a href="https://msdn.microsoft.com/702e5c42-cc8c-43cf-a0bf-d3e450c031a4">RasSetEapUserData</a>
 

 

