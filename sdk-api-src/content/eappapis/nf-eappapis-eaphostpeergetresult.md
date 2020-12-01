---
UID: NF:eappapis.EapHostPeerGetResult
title: EapHostPeerGetResult function (eappapis.h)
description: Obtains the authentication result for the specified EAP authentication session.
helpviewer_keywords: ["EapHostPeerGetResult","EapHostPeerGetResult function [EAPHost]","eaphost.eaphostpeergetresult","eappapis/EapHostPeerGetResult"]
old-location: eaphost\eaphostpeergetresult.htm
tech.root: eaphost
ms.assetid: e1f0fc05-d9cd-4a37-ba74-89ac9948a292
ms.date: 12/05/2018
ms.keywords: EapHostPeerGetResult, EapHostPeerGetResult function [EAPHost], eaphost.eaphostpeergetresult, eappapis/EapHostPeerGetResult
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
 - EapHostPeerGetResult
 - eappapis/EapHostPeerGetResult
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
 - EapHostPeerGetResult
---

# EapHostPeerGetResult function


## -description

Obtains the authentication result for the specified EAP authentication session.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.

### -param reason [in]

An <a href="/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason">EapHostPeerMethodResultReason</a> enumeration value that specifies the reason code for the authentication result returned in <i>ppResult</i>.

### -param ppResult [out]

A pointer to a <a href="/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason">EapHostPeerMethodResultReason</a> structure that contains the authentication results. EAPHost fills this structure with authentication related information defined in <a href="/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult">EapHostPeerMethodResult</a>.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. Supplicants must refer to this parameter to determine if the authentication was successful. After using the error data, free this memory by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>. The return value does not indicate if the authentication was successful. Supplicants must refer to the <i>ppEapError</i> parameter to determine the authentication result.

If the function fails, the return value should be an appropriate error code from Winerror.h, Raserror.h, or Mprerror.h.

## -remarks

The supplicant calls <b>EapHostPeerGetResult</b> on completion of an authentication, which can occur in any of the following scenarios.
   

<ul>
<li>A call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket">EapHostPeerProcessReceivedPacket</a> returned the <b>EapHostPeerResponseResult</b> action code.</li>
<li> The client timed out and wants to get the result based on the current
   state.</li>
<li> The supplicant received an alternate result, perhaps from a packet on the 
   lower layer.</li>
</ul>

## -see-also

[EAPHost Supplicant Run-time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket">EapHostPeerProcessReceivedPacket</a>