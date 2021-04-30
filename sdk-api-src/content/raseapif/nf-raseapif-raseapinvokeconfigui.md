---
UID: NF:raseapif.RasEapInvokeConfigUI
title: RasEapInvokeConfigUI function (raseapif.h)
description: The RAS connection manager calls the RasEapInvokeConfigUI function to display a dialog to obtain configuration information from the user.
helpviewer_keywords: ["RAS_EAP_FLAG_8021X_AUTH","RAS_EAP_FLAG_GUEST_ACCESS","RAS_EAP_FLAG_ROUTER","RasEapInvokeConfigUI","RasEapInvokeConfigUI callback","RasEapInvokeConfigUI callback function [EAP]","_eap_raseapinvokeconfigui","eap.raseapinvokeconfigui","raseapif/RasEapInvokeConfigUI"]
old-location: eap\raseapinvokeconfigui.htm
tech.root: EAP
ms.assetid: cdd9b081-e654-445e-9383-3665258f5cfa
ms.date: 12/05/2018
ms.keywords: RAS_EAP_FLAG_8021X_AUTH, RAS_EAP_FLAG_GUEST_ACCESS, RAS_EAP_FLAG_ROUTER, RasEapInvokeConfigUI, RasEapInvokeConfigUI callback, RasEapInvokeConfigUI callback function [EAP], _eap_raseapinvokeconfigui, eap.raseapinvokeconfigui, raseapif/RasEapInvokeConfigUI
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
 - RasEapInvokeConfigUI
 - raseapif/RasEapInvokeConfigUI
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
 - RasEapInvokeConfigUI
---

# RasEapInvokeConfigUI function


## -description

The RAS connection manager calls the <b>RasEapInvokeConfigUI</b> function to display a dialog to obtain configuration information from the user. RAS calls 
<b>RasEapInvokeConfigUI</b> when a new phone-book entry is created or an existing phone-book entry is edited, provided that the authentication protocol for the entry provides a configuration user interface.

## -parameters

### -param dwEapTypeId [in]

Specifies the authentication protocol for which to invoke the configuration UI.

### -param hwndParent [in]

Handle to the parent window for the UI dialog.

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
<td width="40%"><a id="RAS_EAP_FLAG_8021X_AUTH"></a><a id="ras_eap_flag_8021x_auth"></a><dl>
<dt><b>RAS_EAP_FLAG_8021X_AUTH</b></dt>
</dl>
</td>
<td width="60%">
Specifies that this session is executing in a wireless context.

</td>
</tr>
<tr>
<td width="40%"><a id="RAS_EAP_FLAG_GUEST_ACCESS"></a><a id="ras_eap_flag_guest_access"></a><dl>
<dt><b>RAS_EAP_FLAG_GUEST_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Specified if the client wants guest access. This flag is normally used in the case of a wireless connection such that if the authentication fails for N number of consecutive tries the wireless client, if configured to request guest access, then does so by passing this flag. The RADIUS server should be setup to permit guest access.

</td>
</tr>
</table>

### -param pConnectionDataIn [in]

Pointer to the connection data currently stored in the phone-book entry. If the phone-book entry does not contain any data, this parameter is <b>NULL</b>.

### -param dwSizeOfConnectionDataIn [in]

Specifies the size of the connection data currently stored in the phone-book entry. If the phone-book entry for this connection does not contain any data, this parameter is  zero.

### -param ppConnectionDataOut [out]

Pointer to a pointer that, on successful return, points to the new connection data to store in the phone-book entry. None of this data should be specific to the current machine; phone-book entries should be portable from machine to machine.

### -param pdwSizeOfConnectionDataOut [out]

Pointer to a <b>DWORD</b> that receives the size of the new connection data to store in the phone-book entry.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function was not able to allocate memory for the configuration data, the return value should be <b>ERROR_NOT_ENOUGH_MEMORY</b>.

If the function fails in some other way, the return value should be an appropriate error code from Winerror.h, Raserror.h, or Mprerror.h.

## -remarks

The DLL that implements 
<b>RasEapInvokeConfigUI</b> and 
<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a> may support more than one authentication protocol. The <i>dwEapTypeId</i> parameter specifies for which protocol to invoke the configuration UI.

RAS stores the connection data returned by 
<b>RasEapInvokeConfigUI</b> in the phone-book entry for the connection on the client computer.

## -see-also

[Client-Side Configuration User Interface](/windows/win32/eap/client-side-configuration-user-interface)



[EAP Functions](/windows/win32/eap/eap-functions)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetidentity">RasEapGetIdentity</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapinvokeinteractiveui">RasEapInvokeInteractiveUI</a>