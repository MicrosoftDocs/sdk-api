---
UID: NF:eappapis.EapHostPeerGetAuthStatus
title: EapHostPeerGetAuthStatus function (eappapis.h)
description: Obtains the supplicant's current EAP authentication status from EAPHost.
helpviewer_keywords: ["EapHostNapInfo","EapHostPeerAuthStatus","EapHostPeerGetAuthStatus","EapHostPeerGetAuthStatus function [EAPHost]","EapHostPeerIdentity","EapHostPeerIdentityExtendedInfo","eaphost.eaphostpeergetauthstatus","eappapis/EapHostPeerGetAuthStatus"]
old-location: eaphost\eaphostpeergetauthstatus.htm
tech.root: eaphost
ms.assetid: cb5ceffb-941f-48ad-9271-111f41adc65b
ms.date: 12/05/2018
ms.keywords: EapHostNapInfo, EapHostPeerAuthStatus, EapHostPeerGetAuthStatus, EapHostPeerGetAuthStatus function [EAPHost], EapHostPeerIdentity, EapHostPeerIdentityExtendedInfo, eaphost.eaphostpeergetauthstatus, eappapis/EapHostPeerGetAuthStatus
req.header: eappapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerGetAuthStatus
 - eappapis/EapHostPeerGetAuthStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerGetAuthStatus
---

# EapHostPeerGetAuthStatus function


## -description

Obtains the supplicant's current EAP authentication status from EAPHost.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.

### -param authParam [in]

An <a href="/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams">EapHostPeerAuthParams</a> enumeration value that specifies the type of EAP authentication data to obtain from EAPHost.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EapHostPeerAuthStatus"></a><a id="eaphostpeerauthstatus"></a><a id="EAPHOSTPEERAUTHSTATUS"></a><dl>
<dt><b>EapHostPeerAuthStatus</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAuthData</i> contains a <a href="/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info">EAPHOST_AUTH_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="EapHostPeerIdentity"></a><a id="eaphostpeeridentity"></a><a id="EAPHOSTPEERIDENTITY"></a><dl>
<dt><b>EapHostPeerIdentity</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAuthData</i> contains a <b>WCHAR</b> buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="EapHostPeerIdentityExtendedInfo"></a><a id="eaphostpeeridentityextendedinfo"></a><a id="EAPHOSTPEERIDENTITYEXTENDEDINFO"></a><dl>
<dt><b>EapHostPeerIdentityExtendedInfo</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAuthData</i> contains a <b>CHAR</b> buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="EapHostNapInfo"></a><a id="eaphostnapinfo"></a><a id="EAPHOSTNAPINFO"></a><dl>
<dt><b>EapHostNapInfo</b></dt>
</dl>
</td>
<td width="60%">
Windows 7 or later: [EapHostPeerNapInfo](/windows/win32/eaphost/eaphostpeernapinfo) structure.

</td>
</tr>
</table>

### -param pcbAuthData [out]

The size, in bytes, of the EAP authentication data buffer pointed to by the <i>ppAuthData</i> parameter.

### -param ppAuthData [out]

A pointer to a pointer to a byte buffer that contains the authentication data from EAPHost. The format of this data depends on the value supplied in <i>authParam</i>.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.

## -see-also

[EAPHost Supplicant Run-Time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)